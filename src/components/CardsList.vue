<script>
import SingleCard from "./SingleCard.vue";

import { store } from "../store"

export default {
    name: "CardsList",
    components: {
        SingleCard,
    },
    data() {
        return {
            store,
        }
    },

}
</script>

<template>
    <SingleCard v-for="singleCard in store.cardsList" :card="singleCard" />
</template>

<style lang="scss" scoped>

</style>