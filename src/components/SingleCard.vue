<script>
export default {
    name: "SingleCard",

    props: {
        card: Object,
    }
}
</script>

<template>
    <div class="card" style="width: calc(100%/5);">
        <div class="card-body">
            <img class="img-fluid" :src="card.card_images[0].image_url" alt="">
            <h5 class="card-title"> {{ card.name }} </h5>
            <h6 class="card-subtitle mb-2 text-muted"> {{ card.archetype }} </h6>
        </div>
    </div>
</template>

<style lang="scss" scoped>
div.card {
    background-color: beige;
}
</style>