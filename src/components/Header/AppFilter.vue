<script>
import { store } from '../../store.js';
export default {
    name: 'AppFilter',
    data() {
        return {
            store
        }
    }
}
</script>

<template>

    <!-- <form action="" @submit.prevent="$emit('search')"> -->
    <select @change="updateSelect" v-model="store.archetypeValue" class="form-select my-3"
        aria-label="Default select example">
        <option selected value="">Alien</option>
        <option value="1">1</option>
    </select>
    <!-- </form> -->

</template>

<style lang="scss" scoped>
select {
    width: 200px;
    margin-left: 35px;
}
</style>