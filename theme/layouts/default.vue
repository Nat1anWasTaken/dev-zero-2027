<script setup lang="ts">
import SitconFrame from '../components/SitconFrame.vue'
</script>

<template>
  <SitconFrame variant="default" tone="paper">
    <div class="sitcon-content"><slot /></div>
  </SitconFrame>
</template>
