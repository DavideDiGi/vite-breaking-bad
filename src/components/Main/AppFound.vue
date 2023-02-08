<script>
export default {
    name: 'AppFound',
    props: {
        gameCardsCount: {
            type: Number,
            default: 0
        }
    }
}
</script>

<template>

    <div class="last-container bg-dark">

        <div class="cards-founded p-3">
            <span class="text-white fw-bold">Found {{ gameCardsCount }} cards</span>
        </div>

    </div>

</template>

<style lang="scss" scoped>

</style>