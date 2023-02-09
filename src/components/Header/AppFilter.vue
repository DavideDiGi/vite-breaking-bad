<script>
import axios from 'axios';
import { store } from '../../store.js';
export default {
    name: 'AppFilter',
    data() {
        return {
            store,
            userChoose: ''
        }
    },
    methods: {
        updateSelect(element) {
            axios
                .get(`https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=${element}`)
                .then((response) => {
                    this.store.archetypeChosen = response.data.data;
                    console.log('digi', response.data.data);
                });

        }
    }
}
</script>

<template>

    <!-- <form action="" @submit.prevent="$emit('search')"> -->
    <select @change="updateSelect(userChoose)" v-model="userChoose" class="form-select my-3"
        aria-label="Default select example">
        <option v-for="element in store.archetypeResults" :value="element.archetype_name">
            {{ element.archetype_name }}
        </option>
    </select>
    <!-- </form> -->

</template>

<style lang="scss" scoped>
select {
    width: 200px;
    margin-left: 35px;
}
</style>