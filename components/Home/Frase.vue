<template>
    <TransitionGroup name="aparicao">
        <div v-if="show" class="container">
            <p>
                {{ frase }}
            </p>
        </div>
    </TransitionGroup>
</template>

<script lang="ts">
export default {
    name: "Frase",
    props: {
        frase: {
            type: String as () => string,
            required: true
        }
    },
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
    justify-content: center;
    margin-top: 10px;
    padding: 5px 20px;
    text-align: center;
}

p {
    color: #545454;
    font-size: 20px;
    font-family: 'Roboto Mono', monospace;
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