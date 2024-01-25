<template>
    <nav>
        <div class="container">
            <img class="logo" src="~/assets/img/Home/logo.png" alt="Logo do Site">
            <button @click="menuAtivado">
                <img v-if="!ativarMenu" class="menu" src="~/assets/img/Home/menu.png" alt="Ícone de um menu hamburguer">
                <img v-if="ativarMenu" class="menu" src="~/assets/img/Home/closedMenu.png"
                    alt="Ícone de um X para fechar o menu">
            </button>
        </div>
        <div class="menuAtivo" :class="{ 'ativo': ativarMenu }">
            <button @click="menuAtivado">
                <img v-if="!ativarMenu" class="menu" src="~/assets/img/Home/menu.png" alt="Ícone de um menu hamburguer">
                <img v-if="ativarMenu" class="menu" src="~/assets/img/Home/closedMenu.png"
                    alt="Ícone de um X para fechar o menu">
            </button>
            <ul>
                <li><a href="#">Página 1</a></li>
                <li><a href="#">Página 2</a></li>
                <li><a href="#">Página 3</a></li>
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
    display: none;
    flex-direction: column;
    padding: 10px;
    height: 100vh;
    text-align: right;
    justify-content: right;
    position: absolute;
    top: 0;
    right: 0;
    background-color: white;
    color: red;
}

.menuAtivo.ativo {
    display: flex;
}
</style>
  