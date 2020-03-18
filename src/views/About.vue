<template>
  <div id="about">
    <router-link :to="{path: '/'}">
      <p>home</p>
    </router-link>
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
  p {
    margin-top: 5%;
    text-align: center;
    color: #2c3e50;
    font-size: 35px;
    font-weight: 300;
    cursor: pointer;
    text-decoration: none; 
  }
</style>