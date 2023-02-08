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

        <div class="container-flexed d-flex flex-wrap justify-content-between">
            <div class="card-container border mb-3" v-for="card in store.results">

                <AppCards :card="card" />

            </div>
        </div>
    </div>


</template>

<style lang="scss" >
.container.bg-white {
    width: 87%;
}

.card-container {
    width: calc((100% / 5) - 20px);
    background-color: red;
}
</style>