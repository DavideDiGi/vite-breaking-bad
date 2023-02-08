<script>
// import axios from 'axios';
import AppHeader from './components/Header/AppHeader.vue';
import AppMain from './components/Main/AppMain.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
  },
  data() {
    return {
      gameCards: []
    }
  },
  // created() {

  //   axios
  //     .get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
  //     .then((response) => {

  //       // console,log(response.data.results.slice(0, 20));
  //     });
  // }
}
</script>

<template>

  <AppHeader />

  <AppMain />

</template>

<style lang="scss">
@import './styles/main.scss';

body {
  background-color: orange;
}
</style>
