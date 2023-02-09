<script>
import axios from 'axios';
import { store } from './store'
import AppHeader from './components/Header/AppHeader.vue';
import AppMain from './components/Main/AppMain.vue';
import AppFound from './components/Main/AppFound.vue';


export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFound,

  },
  data() {
    return {
      store
    }
  },

}
</script>

<template>

  <AppHeader />

  <div class="container bg-white pt-5 px-5">
    <AppFound />
  </div>
  <AppMain />

</template>

<style lang="scss">
@import './styles/main.scss';

body {
  background-color: orange;

}
</style>
