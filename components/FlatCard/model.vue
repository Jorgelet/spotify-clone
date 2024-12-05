<script setup lang="ts">
const props = defineProps<{
  src: string;
  title: string;
}>()
</script>

<template>
  <div class="fc-card">
    <Image 
      :src="props.src"
      width="64"
      height="64"
    />
    <div class="fc-container">
      <p class="fc-container-paragraph">
        {{ props.title }}
      </p>
    </div>
    <PlayButton class="play-button"/>
  </div>
</template>

<style scoped>
.fc-card {
  display: flex;
  width: 100%;
  height: auto;
  gap: 14px;
  background-color: hsla(0, 0%, 100%, 0.14);
  align-items: center;
  border-radius: 4px;
  position: relative;
  cursor: pointer;

  &:hover {
    background-color: hsla(0, 0%, 100%, 0.24);

    & .play-button {
      display: flex;
    }
  }
}

img {
  border-radius: 4px;
}

.play-button {
  position: absolute;
  right: 10px;
  color: #000;
}

.fc-container {
  flex: 1;
  overflow: hidden;
}

.fc-container-paragraph {
  font-size: 0.9rem;
  word-break: break-word;
  overflow-wrap: break-word;

  @media (max-width: 768px) {
    font-size: 0.8rem;
  }
}
</style>