<script>
    import axios from 'axios';
    import { store } from './store.js';
    import AppHeader from './components/AppHeader.vue';
    import AppMain from './components/AppMain.vue';

    export default {
        components: {
            AppHeader,
            AppMain
        },
        data () {
           return {
	          store
           };
        },
        methods: {
        getCardsFromApi() {
            // Preparo i parametri della query, per esempio
            const queryParams = {
                num: 20,
                offset: 0 
            };
            //Faccio la chiamata axios con anche i parametri
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
                params:queryParams
            })
            //Popoliamo lo store con i dati dell'api
            .then((response) => {
                store.cards = response.data.data;
            });
        }
    },
        mounted() {
            this.getCardsFromApi();
        }
    };
</script>

<template>
    <AppHeader></AppHeader>
    <AppMain></AppMain>
</template>

<style lang="scss">
    @use './styles/generics';
</style>
