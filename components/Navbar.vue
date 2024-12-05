<template>
  <nav class="nav">
    <a 
      href="/" 
      class="nav-icon">
        <IconsSpotifyDarkLogo />
    </a>
    <div class="nav-search">
      <button 
        class="nav-search--btn" 
        aria-label="Inicio" 
        aria-hidden="false" 
        title="Inicio">
          <IconsHome />
      </button>
      <div 
        class="nav-search-container" 
        aria-label="Buscar" 
        aria-hidden="false" 
        title="Buscar">
          <IconsSearch class="nav-search-container--icon" />
        <input 
          type="search" 
          name="q" 
          placeholder="¿Qué quieres reproducir?" 
          class="nav-search-container--input" 
        />
      </div>
    </div>
    <div class="nav-account">
      <IconsBell />
      <button 
        class="nav-account--btn" 
        title="Usuario" >
        J
      </button>
    </div>
  </nav>
</template>

<style scoped>
.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  grid-area: nav;
  margin-inline: 6px;
  padding: 20px;
  height: 8vh;
  background-color: #000000;
  margin-top: 8px;
}
.nav-search {
  display: flex;
  align-items: center;
  gap: 10px;

  @media (max-width: 768px) {
    display: none;
  }
}
.nav-search--btn {
  cursor: pointer;
  color: #b3b3b3;
  height: 48px;
  width: 48px;
  text-align: center;
  border-radius: 50%;
  border-style: none;
  background-color: #1f1f1f;
}
.nav-search-container {
  display: flex;
  align-items: center;
  position: relative;
  background-color: #1f1f1f;
  border-radius: 500px;
}
.nav-search-container--input {
  background-color: #1f1f1f;
  padding-left: 48px;
  border-style: none;
  width: 600px;
  box-shadow: none;
  border-radius: 500px;
  height: 48px;
  color: #fff;
  font-size: 14px;
  caret-color: #fff;
  text-overflow: ellipsis;
  font-size: 16px;

  &:focus {
    box-shadow: inset 0 0 0 2px #fff;
    outline: none;
  }

  &:focus-visible {
    outline-offset: 0;
  }
}
.nav-search-container--icon {
  position: absolute;
  left: 8px;
}
.nav-account {
  display: flex;
  align-items: center;
  gap: 40px;

  @media (max-width: 768px) {
    display: none;
  }
}
.nav-account--btn {
  cursor: pointer;
  border: none;
  background-color: rgb(255, 100, 55);
  border-radius: 50%;
  color: rgb(0, 0, 0);
  line-height: 32px;
  font-weight: bold;
  height: 32px;
  width: 32px;
  box-shadow: #1f1f1f 0px 0px 2px 12px;
}
</style>