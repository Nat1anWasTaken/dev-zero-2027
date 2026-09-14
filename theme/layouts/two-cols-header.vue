<script setup lang="ts">
import SitconColumns from '../components/SitconColumns.vue'
</script>

<template>
  <SitconColumns header>
    <template v-for="(_, name) in $slots" #[name]><slot :name="name" /></template>
  </SitconColumns>
</template>
