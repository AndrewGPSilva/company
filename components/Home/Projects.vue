<template>
    <div class="container">
        <div class="containerImagens" v-if="lado === 'left'">
            <div class="imagemPost">
                <a :href="href" target="_blank"><img :src="srcImagem" :alt="altImagem" /></a>
            </div>
            <div class="imagemTech">
                <img :src="srcIconUm" :alt="altIconUm" />
                <img :src="srcIconDois" :alt="altIconDois" />
                <img :src="srcIconTres" :alt="altIconTres" />
            </div>
        </div>
        <div class="containerImagensDireita" v-if="lado === 'right'">
            <div class="imagemTechDireita">
                <img :src="srcIconUm" :alt="altIconUm" />
                <img :src="srcIconDois" :alt="altIconDois" />
                <img :src="srcIconTres" :alt="altIconTres" />
            </div>
            <div class="imagemPost">
                <a :href="href" target="_blank"><img :src="srcImagem" :alt="altImagem" /></a>
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
        },
        lado: {
            type: String as () => string,
            required: true
        },
        href: {
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
    padding-top: 5px;
}

img {
    cursor: pointer;
}

.containerImagens, .containerImagensDireita {
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
    border-left: 2px solid black;
}

.imagemTech img {
    margin-left: 10px;
    width: 55px;
    height: 55px;
}

.imagemTechDireita {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-right: 2px solid black;
}

.imagemTechDireita img {
    margin-right: 10px;
    width: 55px;
    height: 55px;
} 
</style>