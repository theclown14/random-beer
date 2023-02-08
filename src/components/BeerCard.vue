<template>
    <div>
        <!-- <div v-if="beer.rating > 1"> -->
        <h1>Бренд</h1>
        <h2>{{ beer.brand }}</h2>
        <h1>Название</h1>
        <h2>{{ beer.name }}</h2>
        <h1>Стиль</h1>
        <h2>{{ beer.style }}</h2>
        <h1>Процент алкоголя</h1>
        <h2>{{ beer.alcohol }}</h2>
        <span v-if="beer.alcohol > '7.0%'">Крепкое пиво</span>
        <span v-else>Легкое пиво</span>
        <h1>Рейтинг</h1>
        <h2>{{ beer.rating }}</h2>
        <!-- </div> -->
    </div>
</template>

<script>

export default {
    props: {
        beer: {
            type: Object,
            required: true,
        },
    },
}
</script>

<style lang="scss" scoped>
@import "@/assets/styles/beer-card.scss";
</style>