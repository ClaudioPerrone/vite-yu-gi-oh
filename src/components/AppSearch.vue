<script>
    import axios from 'axios';
    import { store } from '../store.js';

    export default {
		name: "AppSearch",
        data () {
            return {
                archetypes: [],
            };
        },
        methods: {
            getArchetypesFromApi() {
                axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
                .then((response) => {
                    console.log(response.data);
                    this.archetypes = response.data;
                });
            }
        },
        mounted () {
            this.getArchetypesFromApi();
        }
	}
</script>

<template>
    <div>
        <select>
            <option value="">scegli l'archetipo</option>

            <option v-for="archetype in archetypes" :value="archetype.archetype_name">{{ archetype.archetype_name }}</option>
        </select>
    </div>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables' as *;

    div {  
        padding-bottom: 20px;
        padding-left: 95px;

        select {
            padding: 5px 15px;
        }
    }
</style>