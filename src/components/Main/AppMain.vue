<script>
import AppFound from './AppFound.vue';
import AppCards from './AppCards.vue';

export default {
    name: 'AppMain',
    components: {
        AppFound,
        AppCards
    },
}
</script>

<template>

    <div class="container bg-white p-5">
        <AppFound />

        <div class="container-flexed d-flex flex-wrap justify-content-between">
            <AppCards />
        </div>
    </div>


</template>

<style lang="scss" scoped>

</style>