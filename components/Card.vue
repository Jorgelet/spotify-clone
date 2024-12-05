<script setup lang="ts">
const props = defineProps<{
  src: string;
  alt: string;
  description: string;
}>()
</script>

<template>
  <article class="card">
    <div class="card-image">
      <Image 
        :alt="props.alt"
        :src="props.src"
        height="200"
        width="200"
      />
      <PlayButton class="play-button"/>
    </div>
    <div class="card-paragraph">
      <small class="card-paragraph--text">
        {{ props.description }}
      </small>
    </div>
  </article>
</template>

<style scoped>
.card-paragraph--text {
  font-size: 1rem;

  @media (max-width: 576px) {
    font-size: 0.75rem;
  }
}
.card-paragraph {
  padding: 8px 0;
}

.card-image {
  position: relative;
}
.card {
  border-radius: 4px;
  padding: 16px 16px 0;  

  &:hover {
  background-color: hsla(0, 0%, 100%, 0.24);
  cursor: pointer;
  
  & .play-button {
    transform: translateY(0);
    opacity: 1;  
  }}
}
.play-button {
  position: absolute;
  right: 10px;
  bottom: 8px;
  color: #000;
  display: flex;
  transform: translateY(40%);
  opacity: 0;
  transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out;
}
</style>