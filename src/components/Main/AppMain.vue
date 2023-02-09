<script>
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
}

</script>

<template>

    <div class="container bg-white px-5">

        <AppCards />

    </div>

</template>

<style lang="scss" >

</style>