<template>
    <section class="container" v-if="lado === 'right'">
        <div class="containerTexto">
            <p>
                {{ frase }}
            </p>
        </div>
        <div>
            <img :src="src" :alt="alt" />
        </div>
    </section>
    <section class="container" v-if="lado === 'left'">
        <div>
            <img :src="src" :alt="alt" />
        </div>
        <div class="containerTexto">
            <p>
                {{ frase }}
            </p>
        </div>
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
</style>