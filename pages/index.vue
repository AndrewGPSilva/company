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
        <HomeBtnContact />
        <HomeProjects 
            srcImagem="https://m.media-amazon.com/images/I/B13h1EXqDiS.jpg" 
            altImagem="Imagem da tela inicial da Netflix" 
            srcIconUm="https://i.ibb.co/f27wdz5/spring.png"
            altIconUm="Icone da logo do framework Spring" 
            srcIconDois="https://i.ibb.co/WnqxL8d/html.png"
            altIconDois="Icone da logo do HTML"  
            srcIconTres="https://i.ibb.co/bFXpr1R/css.png"
            altIconTres="Icone da logo do CSS" 
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