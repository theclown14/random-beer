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
img {
  width: 300px;
  height: 200px;
}
</style>
