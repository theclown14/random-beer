<template>
  <div id="app">
    <img src="./assets/beer.jpg" alt="">
    <BeerData />
  </div>
</template>

<script>
import BeerData from './components/BeerData.vue'

export default {
  name: 'App',
  components: {
    BeerData
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

img {
  width: 300px;
  height: 200px;
}
</style>
