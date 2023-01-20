<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import ShopBar from './components/ShopBar.vue';

export default {
    components: { AppHeader, AppMain, ShopBar }
}

</script>

<template>
    <AppHeader />
    <AppMain />
    <ShopBar />
</template>

<style lang="scss">
@use './assets/styles/style.scss';
</style>
