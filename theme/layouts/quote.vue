<script setup lang="ts">
import SitconFrame from '../components/SitconFrame.vue'
</script>

<template>
  <SitconFrame variant="quote" tone="mist">
    <div class="sitcon-content"><slot /></div>
  </SitconFrame>
</template>
