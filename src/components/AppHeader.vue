<script>
export default {
    data() {
        return {
            list: [
                {
                    label: 'characters',
                    url: '#',
                    active: false
                },
                {
                    label: 'comics',
                    url: '#',
                    active: true
                },
                {
                    label: 'movies',
                    url: '#',
                    active: false
                },
                {
                    label: 'tv',
                    url: '#',
                    active: false
                },
                {
                    label: 'games',
                    url: '#',
                    active: false
                },
                {
                    label: 'collectibles',
                    url: '#',
                    active: false
                },
                {
                    label: 'videos',
                    url: '#',
                    active: false
                },
                {
                    label: 'fans',
                    url: '#',
                    active: false
                },
                {
                    label: 'news',
                    url: '#',
                    active: false
                },
                {
                    label: 'shop',
                    url: '#',
                    active: false
                }

            ]
        }
    },
}
</script>

<template lang="">
    <header class="container">
        <a href="/" class="logo">
            <img src="../assets/images/dc-logo.png" alt="">
        </a>
        <nav>
            <ul>
                <li v-for="(item, index) in list" :key="index">
                    <a :href="item.url">{{ item.label }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

header {
    padding: 1rem;
    @include space-between;

    img {
        width: 80px;
    }

    nav {
        height: 80px;

        ul {
            text-transform: uppercase;
            height: 100%;
            display: flex;

            li a {
                display: flex;
                align-items: center;
                font-size: 15px;
                font-weight: 700;
                padding: 0rem 1rem;
                height: 100%;
                border-bottom: 5px solid $white;
                color: $black;

                &:hover {
                    color: $light-blue;
                    border-bottom: 5px solid $light-blue;
                }
            }
        }
    }
}
</style>