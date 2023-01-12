<script>
export default {
    data() {
        return {
            list: [
                {
                    image: 'buy-comics-digital-comics.png',
                    label: 'digital comics',
                    url: '#'
                },
                {
                    image: 'buy-comics-merchandise.png',
                    label: 'dc merchandise',
                    url: '#'
                },
                {
                    image: 'buy-comics-subscriptions.png',
                    label: 'subscription',
                    url: '#'
                },
                {
                    image: 'buy-comics-shop-locator.png',
                    label: 'comic shop locator',
                    url: '#'
                },
                {
                    image: 'buy-dc-power-visa.svg',
                    label: 'dc power visa',
                    url: '#'
                },
            ]
        }
    },

}
</script>

<template lang="">
    <footer>
        <div class="top-footer">
            <div class="container">
                <ul>
                    <li v-for="(item, index) in list" :key="index">
                        <img :src="`/${item.image}`" alt="">
                        <a :href="item.url">
                            {{ item.label }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
        <div class="content-footer">
            <div class="container">
                <div class="footer-links">
                    <div class="links">
                        <h2>DC COMICS</h2>
                        <nav>
                            <ul>
                                <li><a href="#">Characters</a></li>
                                <li><a href="#">Comics</a></li>
                                <li><a href="#">Movies</a></li>
                                <li><a href="#">TV</a></li>
                                <li><a href="#">Games</a></li>
                                <li><a href="#">Videos</a></li>
                                <li><a href="#">News</a></li>
                            </ul>
                        </nav>
                        <h2>SHOP</h2>
                        <nav>
                            <ul>
                                <li><a href="#">Shop DC</a></li>
                                <li><a href="#">Shop DC Collectibles</a></li>
                            </ul>
                        </nav>
                    </div>
                    <div class="links">
                        <h2>DC</h2>
                        <nav>
                            <ul>
                                <li><a href="#">Terms Of Use</a></li>
                                <li><a href="#">Privacy policy (New)</a></li>
                                <li><a href="#">Ad Chois</a></li>
                                <li><a href="#">Advertising</a></li>
                                <li><a href="#">Jobs</a></li>
                                <li><a href="#">Subscriptions</a></li>
                                <li><a href="#">Talent Workshop</a></li>
                                <li><a href="#">CPSC Cerification</a></li>
                                <li><a href="#">Ratings</a></li>
                                <li><a href="#">Shop Help</a></li>
                                <li><a href="#">Contacts Us</a></li>
    
                            </ul>
                        </nav>
                    </div>
                    <div class="links">
                        <h2>SITES</h2>
                        <nav>
                            <ul>
                                <li><a href="#">DC</a></li>
                                <li><a href="#">Mad Magazine</a></li>
                                <li><a href="#">DC Kids</a></li>
                                <li><a href="#">DC Universe</a></li>
                                <li><a href="#">DC Power Visa</a></li>
                            </ul>
                        </nav>
                    </div>
                </div>
                <div class="footer-image">
                    <img src="/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>
        <div class="bottom-footer">
            <div class="container">
                <a href="#">SIGN-UP NOW</a>
                <nav>
                    <h2>FOLLOW US</h2>
                </nav>
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

footer {
    background-color: $light-blue;

    .top-footer {
        position: relative;
        z-index: 1;

        img {
            width: 50px
        }

        ul {
            list-style-type: none;
            padding: 2rem 1rem;
            @include space-between;

            li {
                display: flex;
                align-items: center;

                a {
                    text-transform: uppercase;
                    color: $white;
                    text-decoration: none;
                    padding: 0 0.5rem;
                }
            }

        }
    }

    .content-footer {
        background-image: url('/footer-bg.jpg');
        background-size: cover;

        .container {
            position: relative;
            padding: 2rem 0;
            @include space-between;

            .footer-links {
                display: flex;

                .links {
                    margin-right: 2rem;

                    ul {
                        list-style-type: none;

                        li a {
                            text-decoration: none;
                            color: $grey;

                            &:hover,
                            &:active {
                                color: $white
                            }
                        }
                    }

                    h2 {
                        color: $white;
                        padding: 1rem 0;
                    }
                }
            }

            .footer-image {
                img {
                    position: absolute;
                    top: 0;
                    right: 0;
                    transform: translateY(-15%);
                }
            }

        }

    }

    .bottom-footer {
        background-color: #303030;
        position: relative;
        z-index: 1;

        .container {
            height: 100px;
            @include space-between;

            a {
                text-decoration: none;
                font-size: 20px;
                font-weight: 400;
                padding: 0.5rem 1rem;
                color: $white;
                border: 2px solid $light-blue;

                &:hover,
                &:active {
                    background-color: $light-blue;
                }
            }

            h2 {
                color: $light-blue;
            }

        }
    }
}
</style>