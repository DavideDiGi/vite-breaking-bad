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

    <form action="">
        <select v-model="store.statusValue" class="form-select my-3" aria-label="Default select example">
            <option selected value="">Alien</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
        </select>
    </form>

</template>

<style lang="scss" scoped>
select {
    width: 200px;
    margin-left: 35px;
}
</style>