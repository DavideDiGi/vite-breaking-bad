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
                    console.log('archetype scelta array', response.data.data);
                });

        }
    }
}
</script>

<template>
    <div class="select-box">
        <div class="info">
            Seleziona un Archetype per visualizzare le carte!
        </div>
        <select @change="updateSelect(userChoose)" v-model="userChoose" class="form-select my-3"
            aria-label="Default select example">
            <option v-for="element in store.archetypeResults" :value="element.archetype_name">
                {{ element.archetype_name }}
            </option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
.select-box {
    position: relative;
    padding-top: 10px;

    .info {
        font-size: 0.6rem;
        font-weight: bold;
        position: absolute;
        margin-left: 15px;
    }

    select {
        width: 200px;
        margin-left: 35px;
    }
}
</style>