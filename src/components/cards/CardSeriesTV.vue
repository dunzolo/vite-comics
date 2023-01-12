<script>
export default {
    props: {
        series_card: Object
    }
}
</script>

<template lang="">
    <div class="card">
        <div class="card-image">
            <img :src="series_card.thumb" alt="">
        </div>
        <div class="card-title">
            <span>{{ series_card.series}}</span>
        </div>
    </div>
</template>

<style lang="scss">
@use '/src/styles/partials/variables' as *;

.card {
    width: calc(100% / 6);
    padding: 1rem;
    display: flex;
    flex-direction: column;

    img {
        object-position: left top;
        object-fit: cover;
        width: 100%;
        height: 150px;
    }

    .card-title {
        color: $white;
        text-transform: uppercase;
    }
}
</style>