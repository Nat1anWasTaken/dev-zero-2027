<script setup lang="ts">
import SitconFrame from './SitconFrame.vue'
defineProps<{ header?: boolean; layoutClass?: string; class?: string }>()
</script>

<template>
  <SitconFrame :variant="header ? 'two-cols-header' : 'two-cols'">
    <div class="sitcon-columns" :class="layoutClass">
      <div v-if="header" class="sitcon-column-header"><slot /><slot name="header" /></div>
      <div class="sitcon-column-left sitcon-content" :class="$props.class">
        <slot v-if="!header" />
        <slot name="left" />
      </div>
      <div class="sitcon-column-right sitcon-content" :class="$props.class"><slot name="right" /></div>
      <div v-if="header" class="sitcon-column-bottom"><slot name="bottom" /></div>
    </div>
  </SitconFrame>
</template>
