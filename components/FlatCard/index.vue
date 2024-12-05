<script setup lang="ts">
const flatCard = [
  {
    title: 'Canciones que te gustan',
    src: 'https://misc.scdn.co/liked-songs/liked-songs-640.png'
  },
  {
    title: 'DJ',
    src: 'https://lexicon-assets.spotifycdn.com/DJ-Beta-CoverArt-300.jpg'
  },
  {
    title: 'Descubrimiento semanal',
    src: 'https://newjams-images.scdn.co/image/ab676477000033ad/dt/v3/discover-weekly/7r4_t5l8LlweIDWI6dYHPA==/OTE0LXNlOTE0LXNlOTE0LQ=='
  },
  {
    title: 'Tu biblioteca',
    src: 'https://t.scdn.co/images/728ed47fc1674feb95f7ac20236eb6d7.jpeg'
  },
  {
    title: 'Estaciones',
    src: 'https://image-cdn-fa.spotifycdn.com/image/ab67706c0000da84acd5624ee67079fd8ba7a3e0'
  },
  {
    title: 'Artistas',
    src: 'https://i.scdn.co/image/ab6761610000f178f938ecb6e234ff3339399cf9'
  },
  {
    title: 'Podcasts',
    src: 'https://i.scdn.co/image/ab67656300005f1f71b6c548f19ab782a06a0966'
  },
  {
    title: 'Tus episodios',
    src: 'https://misc.spotifycdn.com/your-episodes/SE-300.png'
  },
]
</script>

<template>
  <div class="fc-section">
    <FlatCardModel 
      v-for="item in flatCard" 
      :key="item.title" 
      :title="item.title" 
      :src="item.src" 
    />
  </div>
</template>

<style scoped>
.fc-section {
  margin-top: 40px;
  width: 100%;

  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(2, 64px);
  gap: 12px 14px;

  @media (max-width: 768px) {
    grid-template-columns: repeat(2, minmax(150px, 1fr));
    max-width: 100vw;
  }
}
</style>