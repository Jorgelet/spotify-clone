<template>
  <button 
    class="play-button" 
    title="Reproducir">
      <IconsPlay class="play-icon"/>
  </button>
</template>

<style scoped>
.play-button {
  width: 48px;
  height: 48px;
  color: #fff;
  border: none;
  background-color: #1db954;
  border-radius: 50%;
  display: none;
  cursor: pointer;
  align-items: center;
  justify-content: center;
  box-shadow: 0 8px 8px rgba(0,0,0,.3);
}
.play-icon {
  width: 20px;
  height: 20px;
}
</style>