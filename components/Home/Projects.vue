<template>
    <div class="container">
        <p>
            "Construindo o futuro da <br>
            web, hoje. Tecnologia de <br>
            ponta, sites de excelência."
        </p>
        <div class="containerImagens">
            <div class="imagemPost">
                <img :src="srcImagem" :alt="altImagem" />
            </div>
            <div class="imagemTech">
                <img :src="srcIconUm" :alt="altIconUm" />
                <img :src="srcIconDois" :alt="altIconDois" />
                <img :src="srcIconTres" :alt="altIconTres" />
            </div>
        </div>
    </div>
</template>

<script lang="ts">
export default {
    name: "Projects",
    props: {
        srcImagem: {
            type: String as () => string,
            required: true
        },
        altImagem: {
            type: String as () => string,
            required: true
        },
        srcIconUm: {
            type: String as () => string,
            required: true
        },
        srcIconDois: {
            type: String as () => string,
            required: true
        },
        srcIconTres: {
            type: String as () => string,
            required: true
        },
        altIconUm: {
            type: String as () => string,
            required: true
        },
        altIconDois: {
            type: String as () => string,
            required: true
        },
        altIconTres: {
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
    flex-direction: column;
    text-align: center;
    padding-left: 20px;
    padding-right: 20px;
    font-size: 20px;
    padding-top: 5px;
}

p {
    color: #545454;
    font-family: 'Roboto Mono', monospace;
}

.containerImagens {
    display: flex;
    justify-content: center;
    padding: 20px;
    gap: 20px;
}

.imagemPost img {
    border-radius: 30px;
    height: 170px;
    width: 250px;
}

.imagemTech {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-left: 1px solid black;
}

.imagemTech img {
    margin-left: 10px;
    width: 55px;
    height: 55px;
}
</style>