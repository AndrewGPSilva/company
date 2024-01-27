<template>
    <div class="container-contato">
        <a href="https://api.whatsapp.com/send?phone=5511978862185&text=Olá, vim pelo seu projeto music player."
            target="_blank">Contate-nos</a>
    </div>
</template>

<script lang="ts">
export default {
    name: "BtnContact"
}
</script>

<style scoped>
.container-contato {
    display: flex;
    justify-content: center;
    padding: 10px;
}

a {
    background-color: rgb(26, 26, 26);
    padding-top: 8px;
    padding-bottom: 8px;
    padding-left: 30px;
    padding-right: 30px;
    border-radius: 50px;
    cursor: pointer;
    font-family: 'Fugaz One', sans-serif;
    color: white;
    font-size: 26px;
}

a:hover {
    background-color: rgb(0, 161, 27);
    color: black;
}
</style>