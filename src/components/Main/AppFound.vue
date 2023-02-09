<script>
import { store } from '../../store';
export default {
    name: 'AppFound',
    data() {
        return {
            store
        }
    }
}
</script>

<template>

    <div class="last-container bg-dark">

        <div class="cards-founded p-3">
            <span class="text-white fw-bold">Found {{ this.store.archetypeChosen.length }} cards</span>
        </div>

    </div>

</template>

<style lang="scss" scoped>

</style>