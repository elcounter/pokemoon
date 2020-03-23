<template>
  <div id="modal">
    <i class="fas fa-times"></i>
  </div>
</template>

<script>
  export default {
    name: 'Modal'
  }
</script>

<style scoped>
  #modal{
    position: relative;
    width: 30%; 
    height: 80%;
    display: flex;
    margin: auto;
    background-color: rgba(1, 1, 1, 0.8);
    box-shadow: 0px 5px 15px 0px black;
    border-radius: 15px;
  }
  i.fa-times{
    position: absolute;
    top: 3%;
    right: 5%;
    color: snow;
    font-size: 30px;
    cursor: pointer;
  }
  @media screen and (max-width: 500px) {
    #modal{
      width: 90%; 
      height: 70%;
      margin-top: 30%;
    }
  }
</style>