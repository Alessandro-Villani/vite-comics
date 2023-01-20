<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import ShopBar from './components/ShopBar.vue';

export default {
    components: { AppHeader, AppMain, ShopBar, AppFooter }
}

</script>

<template>
    <AppHeader />
    <AppMain />
    <ShopBar />
    <AppFooter />
</template>

<style lang="scss">
@use './assets/styles/style.scss';
</style>
