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
        <div class="container">
            <div class="row">
                <CardSeriesTV v-for="(item, index) in array_seriesTV" :key="index" :series_card="item"/>
            </div>
        </div>
    </main>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;

main {
    background-color: $black;

    .row {
        display: flex;
        flex-wrap: wrap;
    }
}
</style>