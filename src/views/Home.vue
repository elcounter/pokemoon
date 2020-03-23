<template>
  <div id="home">
    <img src="../assets/logo.png" alt="Pokemoon logo">
    <router-link :to="{path: '/About'}">
      <p v-on:click="song">Press to start</p>
    </router-link>
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
    padding-top: 50px;
    text-align: center;
    color: #2c3e50;
    font-size: 35px;
    font-weight: 300;
    cursor: pointer;
    animation: floating 3s ease-in-out infinite;
    transition: all 1s;
    text-shadow: 1px 1px 0 snow;
  }
  a {
    text-decoration: none; 
  }
  img{
    width: 45%;
    display: block;
    margin: 3% auto;
  }
  @media screen and (max-width: 500px) {
    img{
      width: 80%;
      margin: 30% auto;
    }
    p {
    padding-top: 0px;
    }
  }
  @media screen and (max-width: 1024px) and (min-width: 501px){
    img{
      width: 70%;
      margin: 15% auto;
    }
  }
</style>
