<template>
  <div id="about">
    <router-link :to="{path: '/'}">
      <p>home</p>
    </router-link>
    <audio id="backgroundMusic" autoplay loop src="../assets/opening.mp3"></audio>
    <button class="play" v-on:click="play"><i class="fas fa-play"></i></button>
    <button class="pause" v-on:click="pause"><i class="fas fa-pause"></i></button>
  </div>
</template>

<script>
  export default {
    name: 'About',
    methods: {
      play: function () {
        var opening = document.getElementById('backgroundMusic')
        opening.play()
      },
      pause: function () {
        var opening = document.getElementById('backgroundMusic')
        opening.pause()
      },
    }
  }
</script>

<style scoped>
  #about{
    width: 100%; 
    height: 100vh;
    background-image: url("../assets/osselait.gif");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  p{
    margin: 1% 1%;
    color: #2c3e50;
    font-size: 15px;
    font-weight: 300;
    cursor: pointer;
    text-decoration: none; 
  }
  a{
    text-decoration: none; 
  }
  button{
    position: absolute;
    display: block;
    background: none;
    border: none;
    font-size: 30px;
    cursor: pointer;
    outline: none;
    animation: moving 2s ease-in-out infinite;
    transition: all 1s;
  }
  button.pause{
    top: 5%;
    right: 5%;
  }
  button.play{
    top: 5%;
    right: 10%;
  }
  @media screen and (max-width: 500px) {
    button.pause{
      top: 5%;
      right: 5%;
    }
    button.play{
      top: 5%;
      right: 15%;
    }
  }
</style>