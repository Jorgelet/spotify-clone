<script setup lang="ts">
const cards = [
  {
    src: 'https://newjams-images.scdn.co/image/ab67647800003f8a/dt/v3/release-radar/ab6761610000e5eb6278c736f8d0da625d64081c/es',
    alt: 'Release Radar',
    description: 'The best new music every Friday'
  },
  {
    src: 'https://pickasso.spotifycdn.com/image/ab67c0de0000deef/dt/v1/img/daily/1/ab6761610000e5ebe1a911f620f24ffa1c736346/es',
    alt: 'Daily Mix 1',
    description: 'Your daily mix'
  },
  {
    src: 'https://pickasso.spotifycdn.com/image/ab67c0de0000deef/dt/v1/img/daily/2/ab6761610000e5eb68f9f1d20b6ad0f4c4c27ba6/es',
    alt: 'Daily Mix 2',
    description: 'Your daily mix'
  },
  {
    src: 'https://pickasso.spotifycdn.com/image/ab67c0de0000deef/dt/v1/img/daily/4/ab6761610000e5eb744a4243fb6cc938011a98f4/es',
    alt: 'Daily Mix 4',
    description: 'Your daily mix'
  },
  {
    src: 'https://pickasso.spotifycdn.com/image/ab67c0de0000deef/dt/v1/img/daily/5/ab6761610000e5ebc36dd9eb55fb0db4911f25dd/es',
    alt: 'Daily Mix 5',
    description: 'Your daily mix'
  },
  {
    src: 'https://pickasso.spotifycdn.com/image/ab67c0de0000deef/dt/v1/img/daily/6/ab6761610000e5ebcd222b80720653f7309fdcaa/es',
    alt: 'Daily Mix 6',
    description: 'Your daily mix'
  }
]
</script>

<template>
  <section class="section">
    <h2 class="section-title">
      Hecho para USER101
    </h2>
    <div class="section-cards-container">
      <Card 
        v-for="(card, index) in cards" 
        :key="index" 
        :src="card.src" 
        :alt="card.alt" 
        :description="card.description" 
      />
    </div>
  </section>
</template>

<style scoped>
.section-title{
  font-size: 1.5rem;
  margin: 64px 0 24px;
}
.section-cards-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 12px;

  @media (max-width: 575px) {
    grid-template-columns: repeat(2, minmax(150px, 1fr));
  }
  
  @media (576px<=width<=768px) {
    grid-template-columns: repeat(3, minmax(150px, 1fr));
  }
}
</style>