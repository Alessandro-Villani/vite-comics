<script>
export default {
    props: {
        comic: Object
    }
}
</script>

<template>
    <figure class="card">
        <img :src="comic.thumb" :alt="comic.series">
        <figcaption>{{ comic.series }}</figcaption>
    </figure>
</template>

<style scoped lang="scss">
@use '../../assets/styles/partial/variables.scss' as *;

figure {
    padding: 1rem;
    cursor: pointer;
    transition: all 0.5s;
    position: relative;

    &:hover {
        scale: 1.1;
    }

    img {
        display: block;
        width: 100%;
        transition: all 0.5s;
    }

    &:hover img {
        box-shadow: 0 0 5px $blue;
    }

    figcaption {
        color: white;
        text-transform: uppercase;
        font-size: 10px;
        background-color: $black;
        padding-top: 1rem;
        position: absolute;
        left: 1rem;
        right: 1rem;
        top: 70%;
        bottom: 1rem;
        transition: all 0.5s;
    }

}
</style>