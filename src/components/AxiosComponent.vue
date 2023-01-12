<script>
import axios from "axios"
import { store } from "../store"


export default {
    name: AxiosComponent,
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

</template>

<style lang="scss" scoped>

</style>