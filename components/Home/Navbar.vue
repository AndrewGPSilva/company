<template>
    <div class="container">
        <img class="logo" src="~/assets/img/Home/logo.jpg" alt="Logo do Site">
        <img class="menu" src="~/assets/img/Home/menu.png" alt="PNG de um ícone de um menu hamburguer">
    </div>
</template>

<script lang="ts">

export default {
    name: "Navbar"
}

</script>

<style scoped>
    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: #0094FF;
        padding: 25px;
    }

    .logo {
        width: 60px;
        height: 60px;
        border-radius: 50%;
        cursor: pointer;
    }

    .menu {
        width: 40px;
        height: 40px;
        cursor: pointer;
    }
</style>