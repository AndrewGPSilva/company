<template>
    <div class="container">
        <p>Seu Site <br> Sua Marca <br> Sua idéia <br> Nossos códigos! </p>
    </div>
</template>

<script lang="ts">
export default {
    name: "Slogan"
}
</script>

<style scoped>
    .container {
        background-image: url("~/assets/img/Home/fundohome.png");
        background-position: top;
        background-size: cover;
        padding: 20px;
        background-color: #0094FF;
        border-bottom-left-radius: 60px;
        border-bottom-right-radius: 60px;
        margin-top: -5px;
    }

    p {
        font-size: 32px;
        font-weight: bold;
        font-family: 'Courier New', Courier, monospace;
        margin-bottom: 10px;
    }
</style>