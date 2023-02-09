<script>
import axios from 'axios';
import { store } from '../../store'
import AppTitle from './AppTitle.vue';
import AppFilter from './AppFilter.vue';

export default {
    name: 'AppHeader',
    components: {
        AppTitle,
        AppFilter
    },
    data() {
        return {
            store
        }
    },

    created() {

        axios
            .get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
            .then((response) => {

                this.store.results = response.data.data.slice(0, 20);
            });

        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php').then((response) => {

            this.store.archetypeResults = response.data;
            this.store.archetypeResults[1].name = this.store.archetypeResults[1].archetype_name;
            console.log('primo array:', response.data)
        });
    }
}

</script>

<template>

    <AppTitle />

    <div class="container">
        <AppFilter />
    </div>

</template>

<style lang="scss">
.container {
    width: 87%;
}
</style>
