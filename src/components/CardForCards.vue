<script>
    export default {
        name: "CardForCards",
        props: {
            cardInfo: Object
        }
    }
</script>

<template>
    <div class="card col-2">
        <img :src="cardInfo.card_images[0].image_url_small" alt="">
        <div class="text">
            <h4>{{ cardInfo.name }}</h4>
            <p>{{ cardInfo.archetype }}</p>
        </div>
    </div>
</template>

<style scoped lang="scss">

    .card  {
        padding: 5px 10px;
        margin: 10px;
        background-color: orange;
    }
</style>