<template>
    <div class="container">
        <h1>
            Company <br> IT Development
        </h1>
    </div>
    <div class="container-contato">
        <button>
            <a href="https://api.whatsapp.com/send?phone=5511978862185&text=Olá, vim pelo seu projeto music player." target="_blank">Contate-nos</a>
        </button>
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
    text-align: left;
    align-items: center;
    margin: 12px;
    border-radius: 15px;
    padding: 10px;
    background-image: url("~/assets/img/Home/banner.png");
    height: 150px;
    color: white;
    background-size: cover;
}

.container-contato {
    display: flex;
    justify-content: center;
    padding: 10px;
}

button {
    background-color: rgb(26, 26, 26);
    padding-top: 12px;
    padding-bottom: 12px;
    padding-left: 45px;
    padding-right: 45px;
    border-radius: 50px;
    cursor: pointer;
}

a {
    font-family: 'Fugaz One', sans-serif;
    color: white;
    font-size: 30px;
}
</style>