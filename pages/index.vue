<template>
    <Head>
        <Title>GPS.ev - {{ name }}</Title>
    </Head>
    <main>
        <HomeSlogan />
        <HomePost 
        frase="Transformando ideias em presença digital. Seu site, sua marca, nossa expertise!"
        src="https://i.ibb.co/zxFNmvB/postUm.jpg" alt="Imagem do Primeiro Post" lado="right"
        />
        <HomePost 
        frase="Construímos a ponte entre sua visão e a web, criando sites que impressionam."
        src="https://i.ibb.co/bHhV9zC/postDois.webp" alt="Imagem do Segundo Post" lado="left"
        />
    </main>
</template>

<script lang="ts">
export default {
    name: "Home",
    data() {
        return {
            name: "Inicio"
        }
    }
}
</script>