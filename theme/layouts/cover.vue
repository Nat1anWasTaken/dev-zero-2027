<script setup lang="ts">
import SitconFrame from '../components/SitconFrame.vue'
</script>

<template>
  <SitconFrame variant="cover" tone="dark">
    <div class="sitcon-content"><slot /></div>
  </SitconFrame>
</template>
