<script>
import { store } from "../store"

export default {
    data() {
        return {
            store,

        }
    },
}
</script>

<template>
    <div class="col-12">
        <h4 class="mt-3">Found {{ store.cardsList.length }} cards</h4>
    </div>
</template>

<style lang="scss" scoped>
h4 {
    color: aqua;
    font-weight: 700;
}
</style>