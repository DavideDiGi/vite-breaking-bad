<script>
// import AppFound from './AppFound.vue';
import AppCards from './AppCards.vue';

export default {
    name: 'AppMain',
    props: {
        gameCardsList: {
            type: Array,
            default: []
        }
    },
    components: {
        // AppFound,
        AppCards
    },
}
</script>

<template>

    <div class="container bg-white px-5">
        <!-- <AppFound :gameCardsCount="gameCards.length" /> -->

        <div class="container-flexed d-flex flex-wrap justify-content-between">
            <div class="card-container border mb-3" v-for="card in gameCardsList">

                <AppCards :card="card" />

                <!-- <div class="single-card bg-success">Card</div>

                <div class="card-info text-center p-3">
                    <div class="card-name fw-bold text-white">"A" CELL BREEDING DEVICE</div>
                    <div class="card-type mt-3">Alien</div>
                </div> -->

            </div>
            <!-- <AppCards /> -->
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

    // .single-card {
    //     height: 300px;
    // }

    // .card-info {
    //     min-height: 100px;
    //     background-color: orange;
    // }
}
</style>