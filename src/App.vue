<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

import axios from "axios"
import { store } from "./store"


export default {

  components: {
    AppHeader,
    AppMain,
  },

  data() {
    return {
      store,
    }
  },

  methods: {

    getCards() {
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0', {
        params: {

        }
      })
        .then((response) => {
          console.log(response.data.data);
          this.store.cardsList = response.data.data;
        })
        .catch(function (error) {
          console.log(error);
        })
        .then(function () {

        });
    }
  },

  created() {
    this.getCards();
  },
}
</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style lang="scss">
@use "../node_modules/bootstrap/scss/bootstrap.scss" as *;
@use "./styles/general" as *;
@use "./styles/partials/variables" as *;
</style>
