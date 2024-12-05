<script setup lang="ts">
const imgItems = [
  {
    src: 'https://misc.spotifycdn.com/your-episodes/SE-300.png',
    alt: 'Actual playing music',
    width: '48',
    height: '48',
    title: 'Tus episodios'
  },
  {
    src: 'https://i.scdn.co/image/ab67616d000048510464a4a2b1558725d9d97277',
    alt: 'Actual playing music',
    width: '48',
    height: '48',
    title: 'Okupa - WOS'
  }
]
</script>

<template>
  <aside class="aside">
    <header class="aside-header">
      <button 
        class="aside--btn" 
        title="Ampliar tu Biblioteca">
          <IconsLibrary />
      </button>
    </header>
    <ul class="aside-list">
      <li 
        v-for="(img, index) in imgItems" 
        :key="index" 
        class="aside-list--item">
          <button 
            class="aside--btn" 
            :title="img.title">
              <Image 
                :src="img.src" 
                :alt="img.alt" 
                :width="img.width" 
                :height="img.height" 
                class="aside-list--item--img" 
              />
          </button>
      </li>
    </ul>
  </aside>
</template>

<style scoped>
.aside {
  grid-area: aside;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0 12px;
  position: relative;
  margin-left: 6px;
  border-radius: 8px;
  background-color: #121212;
  overflow: hidden;

  & button {
    cursor: pointer;
    background: none;
    border: none;
    padding: 0;
  }

  @media (max-width: 768px) {
    display: none;
  }
}

.aside-header {
  position: absolute;
  top: 24px;
}

.aside-list {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  position: absolute;
  top: 64px;
  height: calc(100% - 64px);
  width: 100%;
  overflow-y: hidden;
  transition: overflow-y 0.3s ease;
}

.aside-list:hover {
  overflow-y: overlay;

  &::-webkit-scrollbar {
    z-index: 10;
  }
}

.aside-list::-webkit-scrollbar {
  width: 2px;
}

.aside-list::-webkit-scrollbar-track {
  background: #1e1e1e;
  border-radius: 4px;
}

.aside-list::-webkit-scrollbar-thumb {
  background: #575757;
  border-radius: 4px;
}

.aside-list::-webkit-scrollbar-thumb:hover {
  background: #8b8b8b;
}

.aside-list--item--img {
  border-radius: 4px;
}
</style>