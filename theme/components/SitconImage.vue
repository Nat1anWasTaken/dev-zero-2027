<script setup lang="ts">
import { computed } from 'vue'
import { resolveAssetUrl } from '@slidev/client'
import SitconFrame from './SitconFrame.vue'

const props = withDefaults(defineProps<{
  image?: string
  alt?: string
  side?: 'left' | 'right' | 'full'
  backgroundSize?: 'cover' | 'contain'
  backgroundPosition?: string
  caption?: string
}>(), { side: 'right', alt: '', backgroundSize: 'cover', backgroundPosition: 'center' })
const src = computed(() => props.image ? resolveAssetUrl(props.image) : undefined)
</script>

<template>
  <SitconFrame :variant="'image-' + side">
    <div class="sitcon-image-composition" :data-side="side">
      <figure class="sitcon-figure">
        <img v-if="src" :src="src" :alt="alt" :style="{ objectFit: backgroundSize, objectPosition: backgroundPosition }">
        <figcaption v-if="caption">{{ caption }}</figcaption>
      </figure>
      <div class="sitcon-image-copy sitcon-content"><slot /></div>
    </div>
  </SitconFrame>
</template>
