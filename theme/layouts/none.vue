<script setup lang="ts">
import SitconFrame from '../components/SitconFrame.vue'
</script>

<template>
  <SitconFrame variant="none" tone="paper" :chrome="false">
    <div class="sitcon-content"><slot /></div>
  </SitconFrame>
</template>
