<script>
export default {
    data() {
        return {
            sections: [
                {
                    name: 'dc comics',
                    links: [
                        {
                            text: 'Characters',
                            url: '#'
                        },
                        {
                            text: 'Comics',
                            url: '#'
                        },
                        {
                            text: 'Movies',
                            url: '#'
                        },
                        {
                            text: 'TV',
                            url: '#'
                        },
                        {
                            text: 'Games',
                            url: '#'
                        },
                        {
                            text: 'Collectibles',
                            url: '#'
                        },
                        {
                            text: 'Videos',
                            url: '#'
                        },
                        {
                            text: 'Fans',
                            url: '#'
                        },
                        {
                            text: 'News',
                            url: '#'
                        },
                        {
                            text: 'Shop',
                            url: '#'
                        },
                    ]
                },
                {
                    name: 'shop',
                    links: [
                        {
                            text: 'Shop DC',
                            url: '#'
                        },
                        {
                            text: 'Shop DC Collectibles',
                            url: '#'
                        },
                    ]
                },
                {
                    name: 'dc',
                    links: [
                        {
                            text: 'Term Of Use',
                            url: '#'
                        },
                        {
                            text: 'Privacy Policy (New)',
                            url: '#'
                        },
                        {
                            text: 'Ad Choices',
                            url: '#'
                        },
                        {
                            text: 'Advertising',
                            url: '#'
                        },
                        {
                            text: 'Jobs',
                            url: '#'
                        },
                        {
                            text: 'Subscriptions',
                            url: '#'
                        },
                        {
                            text: 'Talent Workshops',
                            url: '#'
                        },
                        {
                            text: 'CPSC Certificates',
                            url: '#'
                        },
                        {
                            text: 'Ratings',
                            url: '#'
                        },
                        {
                            text: 'Shop Help',
                            url: '#'
                        },
                        {
                            text: 'Contact Us',
                            url: '#'
                        }
                    ]
                },
                {
                    name: 'sites',
                    links: [
                        {
                            text: 'DC',
                            url: '#'
                        },
                        {
                            text: 'MAD Magazine',
                            url: '#'
                        },
                        {
                            text: 'DC Kids',
                            url: '#'
                        },
                        {
                            text: 'DC Universe',
                            url: '#'
                        },
                        {
                            text: 'DC Power Visa',
                            url: '#'
                        }
                    ]
                }
            ]
        }

    }
}
</script>

<template>
    <footer>
        <div class="footer-top">
            <div class="container">
                <nav>
                    <div v-for="section in sections" :key="section.name" class="link-section">
                        <h3>{{ section.name }}</h3>
                        <ul>
                            <li v-for="link in section.links"><a :href="link.url">{{ link.text }}</a></li>
                        </ul>
                    </div>
                </nav>
                <img src="../assets/img/dc-logo-bg.png" alt="dc-logo-big">
            </div>
        </div>
        <div class="footer-bottom">

        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partial/mixins.scss' as *;
@use '../assets/styles/partial/variables.scss' as *;

footer {
    height: calc(100vh - 400px);

    .footer-top {
        height: calc(100% - 100px);
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        padding: 2rem 0;

        .container {
            height: 100%;
            @include flex(row, space-between, center);

        }

        nav {
            max-height: 100%;
            padding: 0;
            @include flex(column);
            flex-wrap: wrap;

            .link-section {
                margin: 0.5rem 1rem;
            }

            h3 {
                color: white;
                text-transform: uppercase;
                margin-bottom: 0.5rem;
            }

            a {
                color: $lightgray;
                transition: all 0.5s;
                font-size: 14px;

                &:hover {
                    color: white;
                    text-decoration: underline;
                }
            }
        }

        img {
            height: 120%;
            width: auto;
        }
    }

    .footer-bottom {
        height: 100px;
        background-color: $gray;
        position: relative;
        z-index: 1;
    }
}
</style>