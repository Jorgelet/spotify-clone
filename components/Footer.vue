<template>
  <footer class="footer">
    <div class="footer-container">
      <Image 
        src="https://i.scdn.co/image/ab67616d000048510464a4a2b1558725d9d97277"
        alt="Actual playing music"
        width="54"
        height="54"
      />
      <div class="footer-detail">
        <h3 class="detail-song">
          OKUPA
        </h3>
        <p class="detail-author">
          WOS
        </p>
      </div>
    </div>
    <Player />
    <PlayerOptions />
  </footer>
</template>

<style scoped>
.footer {
  padding: 0 12px 12px 12px;
  grid-area: player;
  display: flex;
  justify-content: space-between;
  align-items: center;

  @media (max-width: 768px) {
    flex-direction: column;
    align-items: center;
    gap: 16px;
  }
}

.footer-container {
  display: flex;
  gap: 10px;
  width: 30%;
  & img {
    border-radius: 4px;
  }

  @media (max-width: 768px) {
    display: none;
  }
}

.footer-detail {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 8px;
}

.detail-song {
  font-size: .85rem;
  font-weight: 500;
  margin: 0;
}

.detail-author {
  font-size: .7rem;
  font-weight: 300;
  margin: 0;
}
</style>