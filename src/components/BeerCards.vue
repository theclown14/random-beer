<template>
    <div class="wrapper container">
        <input class="beer-search" type="text" v-model="brand" placeholder="Введите название бренда" />
        <ul class="beer-cards">
            <BeerCard v-for="(beer, index) in BeerBrandSearch" :key="index" :beer="beer" class="beer-card" />
        </ul>
    </div>
</template>

<script>
import BeerCard from "@/components/BeerCard.vue";

export default {
    components: { BeerCard },
    data: function () {
        return {
            brand: '',
        }
    },
    props: {
        beers: {
            type: Array,
            required: true,
        },
    },
    computed: {
        BeerBrandSearch() {
            let beerBrand = this.brand;
            return this.beers.filter(function (beer) {
                if (beerBrand === '') return true;
                else {
                    return (beer.brand.toLowerCase().indexOf(beerBrand) > -1)
                }
            })
        },
        RatingSort() {
            return this.beers.filter(beer => beer.rating > 2)
        }
    },
}
</script>

<style lang="scss" scoped>
@import "@/assets/styles/beer-cards.scss";

.beer-search {
    width: 400px;
    border: 1px solid rgba(64, 64, 64, .2);
    border-radius: 32px;
    padding: 15.5px 20px;
    margin-bottom: 24px;
    cursor: pointer;
    font-weight: 500;
    font-size: 16px;
    line-height: 24px;
    display: flex;
    align-items: center;
    color: #404040;
    background: transparent;
}
</style>