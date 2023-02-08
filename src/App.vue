<script>
// import axios from 'axios';
// import { store } from './store'
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
  // data() {
  //   return {
  //     store
  //   }
  // }
  // created() {

  //   axios
  //     .get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
  //     .then((response) => {

  //       this.store.results = response.data.data.slice(0, 20);
  //       console.log(this.store.results)
  //     });
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
