<template>
  <div id="app">
    <img src="./assets/logo.png" alt="Pokemoon logo">
    <Home msg="Click to start"/>
  </div>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
#app {
  width: 100%;
  height: 100vh;
  font-family: 'Montserrat', sans-serif;
  background-image: url("./assets/background.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
img{
  width: 40%;
  display: block;
  margin: 5% auto;
}
</style>
