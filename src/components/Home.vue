<template>
  <div>
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Home',
  props: {
    msg: String
  }
}
</script>

<style scoped>
h1 {
  text-align: center;
  color: #2c3e50;
  font-size: 35px;
  font-weight: 300;
  cursor: pointer;
}
</style>
