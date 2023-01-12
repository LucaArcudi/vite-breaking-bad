<script>
import axios from "axios"

import { store } from "../store"

import CardsComponent from "./CardsComponent.vue"

export default {

    name: "AppMain",

    components: {
        CardsComponent,
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
    <main>
        <div class="container-lg">
            <div class="row">
                <CardsComponent />
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-color: aqua;

    div.container-lg {
        padding: 4rem 0;

        div.row {
            background-color: white;
        }
    }
}
</style>