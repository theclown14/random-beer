<template>
  <div class="main">
    <div class="wrapper container">
      <div class="beer__wrapper">
        <BeerCards :beers="beers" />
        <BeerFilter />
      </div>
    </div>
  </div>
</template>

<script>
import BeerCards from "@/components/BeerCards.vue";
import BeerFilter from "@/components/BeerFilter.vue";
import data from "@/beers.json"
export default {
  components: { BeerCards, BeerFilter },
  data: function () {
    return {
      beers: data.beers,
    }
  }
}
</script>


<style lang="scss" scoped>

</style>
