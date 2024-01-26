<template>
    <nav>
        <div class="container">
            <img class="logo" src="~/assets/img/Home/logo.png" alt="Logo do Site">
            <button v-if="!ativarMenu" @click="menuAtivado">
                <img class="menu" src="~/assets/img/Home/menu.png" alt="Ícone de um menu hamburguer">
            </button>
        </div>
        <div class="menuAtivo" :class="{ 'ativo': ativarMenu }">
            <button @click="menuAtivado" class="btnMenu">
                <img v-if="ativarMenu" class="menu" src="~/assets/img/Home/closedMenu.png"
                    alt="Ícone de um X para fechar o menu" />
            </button>
            <ul>
                <li>
                    <NuxtLink to="/">Inicio</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/projetos">Projetos</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/orcamentos">Orçamentos</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/sobre">Sobre</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/faq">FAQ</NuxtLink>
                </li>
            </ul>
        </div>
    </nav>
</template>
  
<script lang="ts">
export default {
    name: "Navbar",
    data() {
        return {
            ativarMenu: false
        };
    },
    methods: {
        menuAtivado() {
            this.ativarMenu = !this.ativarMenu;
        }
    }
};
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

.menuAtivo {
    right: -300px;
    flex-direction: column;
    padding: 15px;
    height: 45vh;
    border-top-left-radius: 30px;
    border-bottom-left-radius: 30px;
    text-align: right;
    justify-content: right;
    position: absolute;
    top: 0;
    z-index: 99;
    background-color: rgb(88, 88, 88);
    transition: right 0.5s ease;
}

.menuAtivo ul img {
    width: 30px;
    height: 30px;
}

.btnMenu {
    margin-top: 20px;
}

ul {
    margin-top: 40px;
}

.menuAtivo.ativo {
    display: flex;
    flex-direction: column;
    align-items: center;
    right: 0;
}
</style>
  