<template>
  <div class="player-options player-optional">
    <button 
      title="Cola" 
      aria-label="Cola" 
      aria-hidden="false">
        <IconsQueue class="player-icon queue" />
    </button>
    <div class="player-options-audio">
      <IconsAudio class="player-icon"/>
      <ProgressBar 
        :min="0" 
        :max="100" 
        :value="10"
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
.player-options {
  width: 30%;
  height: 100%;
  color: #fff;
  padding-right: 40px;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 12px;
}
.player-icon {
  color: #b3b3b3;
  cursor: pointer;

  &.queue {
    width: 16px;
    height: 16px;
  }
  &:hover {
    transform: scale(1.08);
    color: #fff;
  }
}
.player-options-audio {
  display: flex;
  width: 80px;
  gap: 8px;
  align-items: center;
  height: 100%;
}
.player-optional {
  @media (max-width: 768px) {
    display: none;
  }
}
</style>