<script>
import AppTitle from './AppTitle.vue';
import AppFilter from './AppFilter.vue';

export default {
    name: 'AppHeader',
    components: {
        AppTitle,
        AppFilter
    }
}
</script>

<template>

    <AppTitle />
    <div class="container">
        <AppFilter />
    </div>

</template>

<style lang="scss">
.container {
    width: 87%;
}
</style>