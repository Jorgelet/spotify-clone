<script setup lang="ts">
useHead({
  htmlAttrs: {
    lang: 'es'
  }
})
</script>

<template>
  <Navbar />
  <Aside />
  <main class="main">
    <ModeCard />
    <FlatCard />
    <MainSection />
  </main>
  <Footer />
  <BottomPopup />
</template>

<style scoped>
.main {
  padding: 12px 12px 0 12px;
  margin-right: 6px;
  border-radius: 8px;
  grid-area: main;

  @media (max-width: 768px) {
    padding: 8px;
    margin-right: 0;
    overflow: hidden;
  }
}
</style>