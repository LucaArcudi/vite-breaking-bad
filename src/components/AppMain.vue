<script>
import CardsComponent from "./CardsComponent.vue"
import CardsFoundNo from "./CardsFoundNo.vue"

import { store } from "../store"


export default {
    name: "AppMain",
    components: {
        CardsComponent,
        CardsFoundNo,
    },

    data() {
        return {
            store,

        }
    },
}
</script>

<template>
    <main>
        <div class="container-lg">
            <div class="row">
                <CardsFoundNo :cardsListLength="store.cardsList.length" />
                <CardsComponent :cardsList="store.cardsList" />
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