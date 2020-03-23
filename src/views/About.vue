<template>
  <div id="about">
    <audio id="backgroundMusic" loop src="../assets/opening.mp3"></audio>
    <button class="play" v-on:click="play"><i class="fas fa-play"></i></button>
    <button class="pause" v-on:click="pause"><i class="fas fa-pause"></i></button>
    <Modal />
  </div>
</template>

<script>
  import Modal from '../components/Modal.vue'
  export default {
    name: 'About',
    components: {
      Modal
    },
    methods: {
      play: function () {
        var opening = document.getElementById('backgroundMusic')
        opening.volume = 0.5
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
    animation: moving 1s ease-in-out;
    transition: all 1s;
  }
  button.pause{
    top: 5%;
    right: 5%;
  }
  button.play{
    top: 5%;
    right: 8%;
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