<script>
export default {
    props: {
        cardsListLength: Number,
    }
}
</script>

<template>
    <div class="col-12">
        <h4 class="mt-3">Found {{ cardsListLength }} cards</h4>
    </div>
</template>

<style lang="scss" scoped>
h4 {
    color: aqua;
    font-weight: 700;
}
</style>