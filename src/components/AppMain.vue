<script>
import CardsComponent from "./CardsComponent.vue"
import CardsFoundNo from "./CardsFoundNo.vue"

export default {
    name: "AppMain",
    components: {
        CardsComponent,
        CardsFoundNo,
    },
}
</script>

<template>
    <main>
        <div class="container-lg">
            <div class="row">
                <CardsFoundNo />
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