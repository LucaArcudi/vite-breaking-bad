<script>
export default {
    name: "AppHeader",
}
</script>

<template>
    <header class="container-fluid">
        <div class="row">
            <div class="col-1">
                <img src="../assets/img/71-713335_yugioh-logo-yu-gi-oh.png" alt="">
            </div>
            <div class="col">
                <h1>Yu-Gi-Oh Api</h1>
            </div>
        </div>

    </header>
</template>

<style lang="scss" scoped>
div.row {
    background-color: white;

    img {
        width: 100px;
    }
}

h1 {
    color: aqua
}
</style>