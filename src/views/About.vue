<template>
  <div id="about">
    <audio id="backgroundMusic" loop src="../assets/main.mp3"></audio>
    <button class="play" v-on:click="play"><i class="fas fa-play"></i></button>
    <button class="pause" v-on:click="pause"><i class="fas fa-pause"></i></button>
    <button class="modalButton" @click="showModal = true">OPEN</button>
    <Modal v-if="showModal" />
  </div>
</template>

<script>
  import Modal from '../components/Modal.vue'
  export default {
    name: 'About',
    components: {
      Modal
    },
    data() {
      return {
        showModal: false
      };
    },
    methods: {
      play: function () {
        var opening = document.getElementById('backgroundMusic')
        opening.play()
      },
      pause: function () {
        var opening = document.getElementById('backgroundMusic')
        opening.pause()
      },
    },
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
  }
  button.pause{
    top: 5%;
    right: 5%;
    animation: moving 1s ease-in-out;
    transition: all 1s;
  }
  button.play{
    top: 5%;
    right: 8%;
    animation: moving 1s ease-in-out;
    transition: all 1s;
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
  @media screen and (max-width: 1024px) and (min-width: 501px){
    button.play{
      top: 5%;
      right: 10%;
    }
  }
</style>