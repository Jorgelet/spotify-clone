<script setup lang="ts">
useHead({
  link: [
    {
      rel: 'stylesheet',
      href: '/reset.css',
    }
  ],
  title: 'Clone web de Spotify',
})
</script>

<template>
  <NuxtLayout name="default">
    <NuxtPage />
  </NuxtLayout>
</template>

<style>
@font-face {
  font-family: 'Gotham';
  src: url(/fonts/Gotham-Black.otf) format('opentype');
  font-weight: 700;
  font-style: bold;
  font-display: swap;
}

@font-face {
  font-family: 'Gotham';
  src: url(/fonts/GothamMedium.ttf) format('truetype');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Gotham';
  src: url(/fonts/GothamLight.ttf) format('truetype');
  font-weight: 300;
  font-style: light;
  font-display: swap;
}

html {
  font-family: 'Gotham', system-ui, sans-serif;
}
</style>