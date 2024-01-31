<template>
    <TransitionGroup name="aparicao">
        <div v-if="show" class="container">
            <h1>
                Company <br> IT Development
            </h1>
        </div>
    </TransitionGroup>
</template>

<script lang="ts">
export default {
    name: "Slogan",
    data() {
        return {
            show: false as boolean
        }
    },
    methods: {
        mostrar() {
            this.show = !this.show
        }
    },
    mounted() {
        this.mostrar()
    }
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

.aparicao-enter-active {
  transition: all 0.5s ease-out;
}

.aparicao-leave-active {
  transition: all 0.5s cubic-bezier(1, 0.5, 0.8, 1);
}

.aparicao-enter-from,
.aparicao-leave-to {
  transform: translateX(20px);
  opacity: 0;
}
</style>