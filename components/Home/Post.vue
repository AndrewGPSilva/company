<template>
    <section class="container" v-if="lado === 'right'">
        <div class="containerTexto">
            <p>
                {{frase}}
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
                {{frase}}
            </p>
        </div>
    </section>
</template>

<script lang="ts">
export default {
    name: "Post",
    props: {
        src: String,
        alt: String,
        frase: String,
        lado: String
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