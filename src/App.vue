<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppJumbotron from './components/AppJumbotron.vue';
import AppMain from './components/AppMain.vue';
import ShopBar from './components/ShopBar.vue';
import { menusData, shopLinks, comicsData } from './data';

export default {
    data() {
        return {
            menusData,
            shopLinks,
            comicsData
        }
    },
    components: { AppHeader, AppMain, ShopBar, AppFooter, AppJumbotron }
}

</script>

<template>
    <AppHeader :navLinks="menusData[0].links" />
    <AppJumbotron />
    <AppMain title="current series" :comicsData="comicsData" />
    <ShopBar :items="shopLinks" />
    <AppFooter :sections="menusData" />
</template>

<style lang="scss">
@use './assets/styles/style.scss';
</style>
