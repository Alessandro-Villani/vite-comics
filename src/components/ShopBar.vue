<script>

export default {
    data() {
        return {
            items: [
                {
                    url: '#',
                    image: 'buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS'
                },
                {
                    url: '#',
                    image: 'buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE'
                },
                {
                    url: '#',
                    image: 'buy-comics-subscriptions.png',
                    text: 'SUBSCRIPTION'
                },
                {
                    url: '#',
                    image: 'buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR'
                },
                {
                    url: '#',
                    image: 'buy-dc-power-visa.svg',
                    text: 'DIGITAL COMICS'
                },

            ]
        }
    },
    methods: {
        getImageUrl(image) {
            return new URL(`../assets/img/${image}`, import.meta.url).href;
        },
    }
}

</script>

<template>
    <section id="shop">
        <div class="container">
            <ul>
                <li v-for="item in items" :key="item.text"><a :href="item.url"><img :src="getImageUrl(item.image)"
                            :alt="item.text" class="me-1"><span>{{
    item.text
                            }}</span></a></li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partial/mixins.scss' as *;
@use '../assets/styles/partial/variables.scss' as *;

#shop {
    height: 150px;
    background-color: $blue;
    @include flex(row, center, center);
    position: relative;
    z-index: 1;

    ul {
        display: flex;
        gap: 2rem;

        a {
            @include flex(row, space-between, center);
            color: white;
            font-weight: bold;
            font-size: 14px;

            img {
                height: 40px;
            }
        }
    }
}
</style>