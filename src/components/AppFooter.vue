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
                    image: 'buy-comics-subscription.png',
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
        <div class="top-footer container">
            <ul>
                <li v-for="(item, index) in list" :key="index">
                    <img :src="`../assets/images/${item.image}`" alt="">
                    <a :href="item.url">
                        {{ item.label }}
                    </a>
                </li>
            </ul>
        </div>
    </footer>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

footer {
    background-color: $light-blue;

    .top-footer {
        ul {
            list-style-type: none;
            @include space-between;

            li a {
                text-transform: uppercase;
                color: $white;
                text-decoration: none;
            }
        }
    }
}
</style>