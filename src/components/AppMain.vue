<script>
import { store } from "../store"



import axios from "axios"

export default {

    name: "AppMain",

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
                <h4 class="mt-3">Found {{ store.cardsList.length }} cards</h4>
                <div v-for="card in store.cardsList" class="card" style="width: calc(100%/5);">
                    <div class="card-body">
                        <img class="img-fluid" :src="card.card_images[0].image_url" alt="">
                        <h5 class="card-title"> {{ card.name }} </h5>
                        <h6 class="card-subtitle mb-2 text-muted"> {{ card.archetype }} </h6>
                        <p class="card-text"> {{ card.desc }} </p>
                    </div>
                </div>


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

            h4 {
                color: aqua;
                font-weight: 700;
            }

            div.card {
                background-color: beige;
            }
        }
    }
}
</style>