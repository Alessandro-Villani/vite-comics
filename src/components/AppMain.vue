<script>
import ProductsCard from './products/ProductsCard.vue';


export default {
    props: {
        title: String,
        comicsData: Array
    },
    components: { ProductsCard }
}

</script>

<template>
    <main>
        <div class="container">
            <h3 class="title">{{ title }}</h3>
            <div class="content">
                <ProductsCard v-for="comic in comicsData" :comic="comic" />
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partial/mixins.scss' as *;
@use '../assets/styles/partial/variables.scss' as *;

main {
    background-color: $black;
    min-height: 150px;
    position: relative;

    .content {
        display: flex;
        flex-wrap: wrap;
        padding: 2rem 0;
    }

    h3 {
        padding: 0.5rem 1rem;
        text-transform: uppercase;
        background-color: $blue;
        color: white;
        position: absolute;
        transform: translateY(-50%);
    }

    p {
        color: white;
        font-size: 30px;
        line-height: 150px;
    }

    .card {
        flex-basis: calc(100% / 6);
    }
}
</style>