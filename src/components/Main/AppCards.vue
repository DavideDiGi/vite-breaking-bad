<script>
export default {
    name: 'AppCards',
    props: {
        card: Object
    }
}
</script>

<template>

    <!-- <div class="card-container border mb-3" v-for="card in 15"> -->

    <div class="single-card "><img :src="card.card_images[0].image_url" :alt="card.name">
    </div>

    <div class="card-info text-center p-3">
        <div class="card-name fw-bold text-white"> {{ card.name }}</div>
        <div class="card-type mt-3">{{ card.archetype }}</div>
    </div>

    <!-- </div> -->

</template>

<style lang="scss" scoped>
// .card-container {
//     width: calc((100% / 5) - 20px);
//     background-color: red;

.single-card {
    height: 300px;
}



.card-info {
    min-height: 120px;
    max-width: 100%;
    background-color: orange;

    .card-name {
        width: 100%;

    }
}


img {
    width: 100%;
    height: 100%;
}
</style>
