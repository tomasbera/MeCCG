<template>
  <div class="main-page">
    <div class="background-image"></div>
    <h1>{{ gameTitle }}</h1>
    <p>{{ gameDescription }}</p>
    <div class="buttons">
      <RouterLink to="/play" class="play-button">
        Play Now
      </RouterLink>
      <router-link to="/about" class="about-button">
        About the Game
      </router-link>
    </div>
  </div>
  <RouterView />
</template>

<script>
import { RouterLink, RouterView } from 'vue-router'

export default {
  name: "MainPage",
  data() {
    return {
      gameTitle: "Middle-earth Collectible Card Game",
      gameDescription:
          "Join the adventure in J.R.R. Tolkien's Middle-earth with MeCCG, the collectible card game that lets you explore the rich lore and characters of this beloved universe. Build your deck, master the game mechanics, and challenge other players in this immersive and strategic game.",
    };
  },
  components: {
    RouterLink,
    RouterView,
  },
};
</script>

<style>
.main-page {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
  font-family: "Cinzel Decorative", serif;
  color: #f7f7f7;
  text-shadow: 2px 2px 2px #000000;
}

.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url("@/assets/rivendell.png");
  background-size: cover;
  background-position: center;
  opacity: 0.5;
  z-index: -1;
}

.main-page h1 {
  font-size: 3rem;
  margin-bottom: 20px;
  text-align: center;
  text-transform: uppercase;
}

.main-page p {
  font-size: 1.5rem;
  max-width: 600px;
  text-align: center;
  margin-bottom: 40px;
  line-height: 1.5;
}

.buttons {
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 20px;
}

.play-button,
.about-button {
  padding: 10px 20px;
  font-size: 1.5rem;
  background-color: #c9aa5f;
  color: #443d38;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  text-transform: uppercase;
  text-shadow: 1px 1px 1px #f7f7f7;
  transition: background-color 0.2s ease-in-out;
}

.play-button:hover,
.about-button:hover {
  background-color: #e5c77e;
}
</style>