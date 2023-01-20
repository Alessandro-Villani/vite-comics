<script>

export default {
    data() {
        return {
            navLinks: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },
            ]
        }
    }
}

</script>

<template>
    <header>
        <nav class="container">
            <div class="nav-left">
                <figure>
                    <a href="">
                        <img src="../assets/img/dc-logo.png" alt="dc-logo">
                    </a>
                </figure>
            </div>
            <div class="nav-rignt">
                <ul>
                    <li v-for="link in navLinks" :key="link.text"><a :href="link.url"
                            :class="{ 'active': link.current }">{{
    link.text
                            }}</a></li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partial/mixins.scss' as *;
@use '../assets/styles/partial/variables.scss' as *;

header {
    height: 100px;

    nav {
        @include flex(row, space-between, center);

        img {
            height: 60px;
        }

        ul {
            @include flex (row, space-between, center);
            gap: 1.5rem;

            a {
                display: inline-block;
                height: 100px;
                line-height: 100px;
                text-transform: uppercase;
                font-weight: bold;
                font-family: "Open Sans Condensed", sans-serif;
                border-bottom: 5px solid transparent;
                transition: all 0.5s;

                &.active,
                &:hover {
                    color: $blue;
                    border-bottom: 5px solid $blue;
                }
            }

        }
    }
}
</style>