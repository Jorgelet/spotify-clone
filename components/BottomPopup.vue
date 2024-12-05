<script setup lang="ts">
const isVisible = ref(true);

function closePopup() {
  isVisible.value = false;
}
</script>

<template>
  <div 
    v-if="isVisible" 
    class="bottom-popup">
      <p>
        Este proyecto es un ejercicio de aprendizaje para practicar desarrollo web. No tiene relación con Spotify.
        Si busca la aplicación oficial, visite el
        <a
          href="https://open.spotify.com/" 
          target="_blank" 
          rel="noopener noreferrer">
            sitio oficial de Spotify
        </a>
      </p>
      <button 
        class="close-button" 
        title="Cerrar"  
        @click="closePopup">
          <IconsClose />
      </button>
  </div>
</template>

<style scoped>
.bottom-popup {
  position: fixed;
  bottom: 0;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  color: #ffffff;
  text-align: center;
  padding: 10px;

  & a {
    color: #1ed760;
  }
}

.close-button {
  background: none;
  border: none;
  color: #1db954;
  cursor: pointer;
  position: absolute;
  right: 40px;
  top: 0;
}
</style>