<script>
// import axios from 'axios';
import AppCards from './AppCards.vue';
import { store } from '../../store.js';

export default {
    name: 'AppMain',
    data() {
        return {
            store
        }
    },
    components: {
        AppCards
    },
    // created() {

    //     axios
    //         .get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
    //         .then((response) => {

    //             this.store.results = response.data.data.slice(0, 20);
    //             console.log(this.store.results)
    //         });

    // }
}

</script>

<template>

    <div class="container bg-white px-5">

        <AppCards />

    </div>

</template>

<style lang="scss" >

</style>