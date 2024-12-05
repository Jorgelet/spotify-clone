<template>
  <div class="layout">
    <slot />
  </div>
</template>

<style scoped>
.layout {
  min-height: 100dvh;
  max-width: 100vw;
  display: grid;
  grid-template-areas:
    "nav nav nav"
    "aside main main"
    "player player player";
  grid-template-columns: 72px 1fr;
  grid-template-rows: auto 1fr auto;
  gap: 4px 10px;
  background-color: #000000;

  @media (max-width: 768px) {
    grid-template-areas:
      "nav nav"
      "main main"
      "player player";
    grid-template-rows: auto 1fr auto;
    grid-template-columns: 1fr;
  }
}
</style>