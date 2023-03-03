<template>
  <div class="starter-packs-page">
    <h1>Select a Starter Pack</h1>
    <div class="starter-packs-container">
      <div class="starter-pack-card">
        <img src="/assets/starter-pack-1.jpg" alt="Starter Pack 1">
        <h2>Starter Pack 1</h2>
        <p>Description of Starter Pack 1</p>
        <router-link to="/gameplay" class="play-button">
          Play Now
        </router-link>
      </div>
      <div class="starter-pack-card">
        <img src="/assets/starter-pack-2.jpg" alt="Starter Pack 2">
        <h2>Starter Pack 2</h2>
        <p>Description of Starter Pack 2</p>
        <router-link to="/gameplay" class="play-button">
          Play Now
        </router-link>
      </div>
      <div class="starter-pack-card">
        <img src="/assets/starter-pack-3.jpg" alt="Starter Pack 3">
        <h2>Starter Pack 3</h2>
        <p>Description of Starter Pack 3</p>
        <router-link to="/gameplay" class="play-button">
          Play Now
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "StarterPacksPage",
};
</script>

<style>
.starter-packs {
display: flex;
flex-wrap: wrap;
justify-content: center;
gap: 20px;
}

.starter-pack {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 300px;
  height: 400px;
  background-color: #4a4d4f;
  color: #f7f7f7;
  text-shadow: 2px 2px 2px #000000;
  box-shadow: 2px 2px 5px #000000;
  padding: 20px;
  box-sizing: border-box;
}

.starter-pack h2 {
  font-size: 2rem;
  margin-bottom: 20px;
}

.starter-pack img {
  width: 200px;
  height: 200px;
  object-fit: contain;
  margin-bottom: 20px;
}

.starter-pack button {
  background-color: #c9aa5f;
  color: #3a3f3d;
  border: none;
  padding: 10px 20px;
  font-size: 1.2rem;
  font-weight: bold;
  text-transform: uppercase;
  letter-spacing: 3px;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.starter-pack button:hover {
  background-color: #f7f7f7;
  color: #c9aa5f;
  box-shadow: 2px 2px 5px #000000;
}
</style>

