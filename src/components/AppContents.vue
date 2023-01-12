<script>
import list_series_tv from './data/listSeriesTV.js';
import CardSeriesTV from './cards/CardSeriesTV.vue';

export default {
    components: {
        CardSeriesTV
    },
    data() {
        return {
            array_seriesTV: list_series_tv
        }
    },
}
</script>

<template lang="">
    <main>
        <div class="jumbotron">
            <img src="../assets/images/jumbotron.jpg" alt="">
        </div>
        <div class="container">
            <span class="top-label-light-blue">Current series</span>
            <div class="row">
                <CardSeriesTV v-for="(item, index) in array_seriesTV" :key="index" :series_card="item"/>
            </div>
            <div class="bottom-btn">
                <button class="btn-light-blue">Load more</button>
            </div>
        </div>
    </main>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.jumbotron {
    img {
        width: 100vW;
        height: 350px;
        object-fit: cover;
        object-position: top;
    }
}

main {
    background-color: $black;

    .top-label-light-blue {
        @include bg-light-blue;
        font-size: 25px;
        font-weight: 700;
        padding: 0.5rem 2rem;
        position: absolute;
        top: 0;
        left: 0;
        transform: translateY(-50%);
    }

    .container {
        position: relative;

        .row {
            padding: 2rem 1rem;
            display: flex;
            flex-wrap: wrap;
        }
    }

    .bottom-btn {
        text-align: center;

        .btn-light-blue {
            @include bg-light-blue;
            padding: 0.5rem 3rem;
            border: none;
            margin-bottom: 1rem;
        }
    }
}
</style>