<script>
    import CardList from './CardList.vue';

    export default {
        name: "AppMain",
        components: {
            CardList
        }
    }
</script>

<template>
    <main>
        <div class="container">
            <CardList></CardList>
        </div>
    </main>
</template>

<style scoped lang="scss">

main {
    background-color: orange;
    height: 100vh;
    padding: 10px;
    
    .container {
        background-color: white;
    }
}
</style>