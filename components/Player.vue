<template>
  <div class="player-container">
    <div class="player">
      <button 
        title="Activar Aleatorio" 
        aria-label="Activar Aleatorio" 
        aria-hidden="false" 
        class="player-optional">
          <IconsRamdom class="player-icon" />
      </button>
      <button 
        title="Anterior" 
        aria-label="Anterior" 
        aria-hidden="false">
          <IconsNext class="player-icon reversed" />
      </button>
      <div 
        class="player-play-button" 
        title="Reproducir" 
        aria-label="Reproducir" 
        aria-hidden="false" 
        role="button">
          <IconsPlay class="player-icon play"/>
      </div>
      <button 
        title="Siguiente" 
        aria-label="Siguiente" 
        aria-hidden="false">
          <IconsNext class="player-icon"/>
      </button>
      <button 
        title="Activar Repetir" 
        aria-label="Activar Repetir" 
        aria-hidden="false" 
        class="player-optional">
          <IconsRepeat class="player-icon"/>
      </button>
    </div>
    <div class="progress-bar player-optional">
      <ProgressBar 
        :min="0" 
        :max="100" 
        :value="50"
      />
    </div>
  </div>
</template>

<style scoped>
button {
  background-color: transparent;
  border: none;
  cursor: pointer;
}
.player-container {
  display: flex;
  flex-direction: column;
  gap: 12px;
  width: 40%;
  height: 100%;
}
.player {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 16px;
}
.player-play-button {
  width: 32px;
  height: 32px;
  display: flex;
  background-color: #fff;
  border-radius: 50%;
  align-items: center;
  justify-content: center;
  cursor: pointer;

  &:hover {
    transform: scale(1.05);
  }
}
.player-icon {
  color: #b3b3b3;
  width: 16px;
  height: 16px;
  cursor: pointer;

  &:hover {
    transform: scale(1.08);
    color: #fff;
  }

  &.reversed {
    transform: rotate(180deg);

    &:hover {
      transform: rotate(180deg) scale(1.08);
    }
  }
  &.play {
    color: #000;

    &:hover {
      transform: none;
    }
  }
}
.player-optional {
  @media (max-width: 768px) {
    display: none;
  }
}
</style>