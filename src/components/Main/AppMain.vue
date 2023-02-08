<script>
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
        AppCards
    },
}
</script>

<template>

    <div class="container bg-white px-5">

        <div class="container-flexed d-flex flex-wrap justify-content-between">
            <div class="card-container border mb-3" v-for="card in gameCardsList">

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