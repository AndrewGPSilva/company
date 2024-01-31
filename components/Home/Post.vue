<template>
    <section class="container" v-if="lado === 'right'">
        <TransitionGroup name="aparicao">
            <div v-if="show" class="containerTexto">
                <p>
                    {{ frase }}
                </p>
            </div>
            <div v-if="show">
                <img :src="src" :alt="alt" />
            </div>
        </TransitionGroup>
    </section>
    <section class="container" v-if="lado === 'left'">
        <TransitionGroup name="aparicao">
            <div v-if="show">
                <img :src="src" :alt="alt" />
            </div>
            <div v-if="show" class="containerTexto">
                <p>
                    {{ frase }}
                </p>
            </div>
        </TransitionGroup>
    </section>
</template>

<script lang="ts">
export default {
    name: "Post",
    props: {
        src: {
            type: String as () => string,
            required: true,
        },
        alt: {
            type: String as () => string,
            required: true,
        },
        frase: {
            type: String as () => string,
            required: true,
        },
        lado: {
            type: String as () => "right" | "left",
            required: true,
        }
    },
    data() {
        return {
            show: false as boolean
        }
    },
    methods:{
        animacao() {
            this.show = !this.show;
        }
    },
    mounted(){
        this.animacao()
    }
}
</script>

<style scoped>
.container {
    display: flex;
    justify-content: center;
    margin-top: 13px;
    padding-left: 20px;
    padding-right: 20px;
    align-items: center;
    gap: 15px;
}

.containerTexto p {
    font-weight: bold;
    font-family: 'Roboto Mono', monospace;
}

img {
    width: 150px;
    height: 130px;
    border-radius: 20px;
}

.aparicao-enter-active {
  transition: all 0.5s ease-out;
}

.aparicao-leave-active {
  transition: all 0.5s cubic-bezier(1, 0.5, 0.8, 1);
}

.aparicao-enter-from,
.aparicao-leave-to {
  transform: translateX(-20px);
  opacity: 0;
}
</style>