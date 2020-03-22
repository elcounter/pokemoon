<template>
  <div id="home">
    <img src="../assets/logo.png" alt="Pokemoon logo">
    <router-link :to="{path: '/About'}">
      <p v-on:click="song">Press to start</p>
    </router-link>
    <img src="../assets/dracofeu.gif" alt="Dracaufeu">
  </div>
</template>

<script>
  export default {
    name: 'Home',
    methods: {
      song: function () {
        const audio =  new Audio('https://play.pokemonshowdown.com/audio/notification.wav');
        audio.play();
      }
    }
  }
</script>

<style scoped>
  #home{
    width: 100%; 
    height: 100vh;
    background-image: url("../assets/background.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  p {
    text-align: center;
    color: #2c3e50;
    font-size: 35px;
    font-weight: 300;
    cursor: pointer;
  }
  a {
    text-decoration: none; 
  }
  img{
    width: 40%;
    display: block;
    margin: 3% auto;
  }
  @media screen and (max-width: 500px) {
    img{
      width: 80%;
      margin: 30% auto;
    }
  }
</style>
