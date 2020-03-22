<template>
  <div id="about">
    <router-link :to="{path: '/'}">
      <p>home</p>
    </router-link>
    <audio id="player" autoplay loop src="../assets/opening.mp3"></audio>
    <button onclick="document.getElementById('player').muted=!document.getElementById('player').muted"><i class="fas fa-music"></i></button>
  </div>
</template>

<script>
  export default {
    name: 'About'
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
    top: 5%;
    right: 5%;
    background: none;
    border: none;
    font-size: 30px;
    cursor: pointer;
    outline: none;
  }
</style>