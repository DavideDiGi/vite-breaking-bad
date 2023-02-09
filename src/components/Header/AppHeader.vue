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
    // computed: {
    //     saveArchetypeName() {
    //         this.store.archetypeResults[1].name = this.store.archetypeResults[1].archetype_name;
    //         console.log('eccoloo' + this.store.archetypeResults[1].name)
    //     }


    created() {

        axios
            .get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
            .then((response) => {

                this.store.results = response.data.data.slice(0, 20);
                // console.log('primo axios: ')
                // console.log(this.store.results)
            });

        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php').then((response) => {

            this.store.archetypeResults = response.data;
            // console.log('secondo axios: ')
            // console.log(this.store.archetypeResults)
            // console.log(this.store.archetypeResults[1].archetype_name)
            this.store.archetypeResults[1].name = this.store.archetypeResults[1].archetype_name;
            // console.log('eccoloo' + this.store.archetypeResults[1].name)
            console.log('davide', response.data)
            // console.log('ecco lo store' + this.store.archetypeResults)
        });
    }
}
    // computed: {
    //     // getArchetypes() {
    //     //     axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php').then((response) => {

    //     //         this.store.archetypeResults = response.data;
    //     //         console.log('secondo axios: ')
    //     //         console.log(this.store.archetypeResults)
    //     //         console.log('ecco lo store' + this.store.archetypeResults)
    //     //     });
    //     // }
    // },

</script>

<template>

    <AppTitle />
    <div>
        Status: {{ store.archetypeValue }}
    </div>
    <div class="container">
        <AppFilter />
    </div>

</template>

<style lang="scss">
.container {
    width: 87%;
}
</style>


<!-- computed: {
    getArchetypes() {
        axios
            .get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            // , {
            //     // params: {
            //     //     archetype: this.store.archetypeValue
            //     // }
            // })
            .then((response) => {

                this.store.archetypeResults = response.data.results;
                console.log('secondo axios: ')
                console.log(this.store.archetypeResults)
            });
        // console.log('eccomi')
        // console.log(this.archetypeValue)
    }
}, -->