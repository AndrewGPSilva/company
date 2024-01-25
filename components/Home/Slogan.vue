<template>
    <div class="container">
        <img src="~/assets/img/Home/persona.png" alt="Personagem masculino usando o computador">
        <h1>
            Seu site, <br> Sua marca
        </h1>
    </div>
</template>

<script lang="ts">
export default {
    name: "Slogan"
}
</script>

<style scoped>
    .container {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 10px;
        background-color: #0094FF;
        border-bottom-left-radius: 60px;
        border-bottom-right-radius: 60px;
        margin-top: -5px;
    }

    .container img {
        width: 200px;
        height: 200px;
    }
</style>