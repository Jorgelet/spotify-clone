<script setup lang="ts">
const props = defineProps({
  min: {
    type: Number,
    default: 0,
  },
  max: {
    type: Number,
    required: true,
  },
  value: {
    type: Number,
    required: true,
  },
});

const percentage = computed(() => {
  return ((props.value - props.min) / (props.max - props.min)) * 100;
});
</script>

<template>
  <div class="progress-bar">
    <div 
      :style="{ width: percentage + '%' }"
      class="progress-bar-fill"
    />
  </div>
</template>

<style scoped>
.progress-bar {
  width: 100%;
  height: 4px;
  background-color: #b3b3b3;
}

.progress-bar-fill {
  height: 100%;
  background-color: #fff;
  width: 0%;
}
</style>