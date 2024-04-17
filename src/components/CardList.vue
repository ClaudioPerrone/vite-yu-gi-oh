<script>
    import { store } from '../store.js';
    import CardForCards from './CardForCards.vue';

    export default {
        name: "CardList",
        components: {
            CardForCards
        },
        data() {
            return {
		        store
            }
        }
    }
</script>

<template>
    <div class="container">
        <div class="row">
            <CardForCards v-for="singleCard in store.cards" :key="singleCard.id" :cardInfo="singleCard"></CardForCards>
        </div>
    </div>
</template>

<style scoped lang="scss">

</style>