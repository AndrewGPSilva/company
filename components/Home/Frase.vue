<template>
    <div class="container">
        <p>
            {{ frase }}
        </p>
    </div>
</template>

<script lang="ts">
export default {
    name: "Frase",
    props: {
        frase: {
            type: String as () => string,
            required: true
        }
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
</style>