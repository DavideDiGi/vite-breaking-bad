<script>
export default {
    name: 'AppCards'
}
</script>

<template>

    <div class="card-container border mb-3" v-for="card in 15">

        <div class="single-card bg-success">Card</div>

        <div class="card-info text-center p-3">
            <div class="card-name fw-bold text-white">"A" CELL BREEDING DEVICE</div>
            <div class="card-type mt-3">Alien</div>
        </div>

    </div>

</template>

<style lang="scss" scoped>
.card-container {
    width: calc((100% / 5) - 20px);
    background-color: red;

    .single-card {
        height: 300px;
    }

    .card-info {
        min-height: 100px;
        background-color: orange;
    }
}
</style>