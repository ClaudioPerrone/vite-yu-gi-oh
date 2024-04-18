<script>
    import CardList from './CardList.vue';
    import AppSearch from './AppSearch.vue';

    export default {
        name: "AppMain",
        components: {
            CardList,
            AppSearch
        }
    }
</script>

<template>
    <main>
        <AppSearch></AppSearch>
        <div class="container">
            <CardList></CardList>
        </div>
    </main>
</template>

<style scoped lang="scss">

main {
    background-color: orange;
    height: 100%;
    padding: 20px 0;
    
    .container {
        background-color: white;
    }
}
</style>