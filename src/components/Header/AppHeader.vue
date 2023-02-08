<script>
import axios from 'axios';
import { store } from '../../store'
import AppTitle from './AppTitle.vue';
import AppFilter from './AppFilter.vue';

export default {
    name: 'AppHeader',
    components: {
        AppTitle,
        AppFilter
    },
    data() {
        return {
            store
        }
    },
    created() {

        axios
            .get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
            .then((response) => {

                this.store.results = response.data.data.slice(0, 20);
                console.log(this.store.results)
            });
    }
}

</script>

<template>

    <AppTitle />
    <!-- <div>
        Status: {{ store.statusValue }}
    </div> -->
    <div class="container">
        <AppFilter />
    </div>

</template>

<style lang="scss">
.container {
    width: 87%;
}
</style>