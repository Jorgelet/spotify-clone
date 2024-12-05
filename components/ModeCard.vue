<script setup lang="ts">
function toggleClass (event: MouseEvent) {
  const active = document.querySelector('.section-mode.active');
  active?.classList.remove('active');
  (event.target as HTMLElement).classList.add('active')
}
</script>

<template>
  <div class="section">
    <span 
      class="section-mode active" 
      @click="toggleClass">
        Todo
    </span>
    <span 
      class="section-mode" 
      @click="toggleClass">
        Música
    </span>
    <span 
      class="section-mode" 
      @click="toggleClass">
        Pódcasts
    </span>
  </div>
</template>

<style scoped>
.section {
  display: flex;
  gap: 8px;
}
.section-mode {
  font-size: .85rem;
  width: fit-content;
  padding: 7px 12px;
  cursor: pointer;
  background-color: hsla(0,0%,100%,.14);
  border-radius: 16px;
  &.active {
    background-color: #fff;
    color: #000;
  }
}
</style>