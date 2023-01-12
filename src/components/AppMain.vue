<script>
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
}
</script>

<template>
    <main>
        <div class="container-lg">
            <div class="row">
                <h4 class="mt-3">Found {{ store.cardsList.length }} cards</h4>
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

            h4 {
                color: aqua;
                font-weight: 700;
            }
        }
    }
}
</style>