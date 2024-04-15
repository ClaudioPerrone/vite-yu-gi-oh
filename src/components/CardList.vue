<script>
    import CardForCards from './CardForCards.vue';
    export default {
        name: "CardList"
    }
</script>

<template>
    <main>
        <div class="container">
            <div class="row">
                <CardForCards></CardForCards>
            </div>
        </div>
    </main>
</template>

<style scoped lang="scss">

main {
    background-color: orange;
    height: 100vh;
}
</style>