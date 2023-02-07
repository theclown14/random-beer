<template>
  <div class="">
    <h1>Пиво brand</h1>
    <h2>{{ beer.brand }}</h2>
    <h1>Пиво name</h1>
    <h2>{{ beer.name }}</h2>
    <h1>Пиво style</h1>
    <h2>{{ beer.style }}</h2>
    <h1>Пиво alcohol</h1>
    <h2>{{ beer.alcohol }}</h2>
    <span v-if="beer.alcohol > '7.0%'">hight</span>
    <span v-else>low</span>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      beer: ""
    }
  },
  mounted() {
    const BeerData = async () => {
      let url = 'https://random-data-api.com/api/beer/random_beer';
      let response = await fetch(url);
      this.beer = await response.json();
    }
    BeerData();
  }
}
</script>


<style scoped>
h1 {
  color: salmon;
}
</style>
