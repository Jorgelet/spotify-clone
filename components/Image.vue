<script setup lang="ts">
const props = defineProps<{
  src: string;
  alt?: string;
  width: string;
  height: string;
  loading?: 'lazy' | 'eager';
}>()
</script>

<template>
<img 
  aria-hidden="false" 
  draggable="false" 
  :loading= "props.loading ?? 'eager'"
  :width="props.width"
  :height="props.height"
  :src="props.src"
  :alt="props.alt ?? ''"
  class="img-component"/>
</template>

<style scoped>
.img-component {
  max-width: 100%;
  height: auto;
}
</style>