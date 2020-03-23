<template>
  <div id="modal">
    <i class="fas fa-times"></i>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minima ipsam corporis tenetur iure quam dolore, illo nihil harum, maiores, eius enim impedit nam. Nulla, blanditiis. Iusto cupiditate consectetur neque nostrum!</p>
    <span>© elcounter 2020</span>
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
    margin-top: 3%;
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
  p{
    color: snow;
    text-align: justify;
    line-height: 30px;
    width: 80%;
    margin: auto;
    font-style: italic;
  }
  span{
    position: absolute;
    bottom: 7px;
    left: 15px;
    font-size: 10px;
    color: grey;
  }
  @media screen and (max-width: 500px) {
    #modal{
      width: 90%; 
      height: 70%;
      margin-top: 30%;
    }
  }
  @media screen and (max-width: 1024px) and (min-width: 501px) {
    #modal{
      width: 80%; 
      height: 70%;
      margin-top: 20%;
    }
    p{
      line-height: 50px;
   }
  }
</style>