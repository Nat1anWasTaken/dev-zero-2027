<script setup lang="ts">
import { computed } from 'vue'
import { handleBackground, useSlideContext } from '@slidev/client'

const props = withDefaults(defineProps<{
  variant?: string
  tone?: 'paper' | 'dark' | 'mist' | 'acid'
  background?: string
  backgroundSize?: string
  backgroundPosition?: string
  eyebrow?: string
  footer?: string | false
  chrome?: boolean
  frontmatter?: Record<string, unknown>
}>(), { variant: 'default', tone: 'paper', chrome: true, footer: undefined, backgroundSize: 'cover', backgroundPosition: 'center' })

const { $slidev, $page, $frontmatter } = useSlideContext()
const config = computed(() => $slidev.configs.themeConfig || {})
// Read the actual frontmatter as well: Slidev consumes some headmatter fields.
const tone = computed(() => $frontmatter.tone || props.tone)
const footer = computed(() => $frontmatter.footer ?? props.footer ?? config.value.footer)
const backgroundStyle = computed(() => ({
  ...handleBackground(props.background, true, props.backgroundSize),
  backgroundPosition: props.backgroundPosition,
}))
</script>

<template>
  <div class="slidev-layout sitcon-frame" :class="'sitcon-' + variant" :data-tone="tone" :style="background ? backgroundStyle : undefined">
    <header v-if="chrome" class="sitcon-header">
      <span class="sitcon-brand">{{ config.brand ?? 'SITCON' }} <span>{{ config.year ?? '2027' }}</span></span>
      <span v-if="$frontmatter.label" class="sitcon-label">{{ $frontmatter.label }}</span>
    </header>
    <main class="sitcon-body">
      <p v-if="eyebrow" class="sitcon-eyebrow">{{ eyebrow }}</p>
      <slot />
    </main>
    <footer v-if="chrome && footer !== false" class="sitcon-footer">
      <span>{{ footer }}</span>
      <span v-if="config.showPageNumber !== false">{{ String($page).padStart(2, '0') }}</span>
    </footer>
  </div>
</template>
