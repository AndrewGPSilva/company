<template>
    <Head>
        <Title>GPF.ev - {{ name }}</Title>
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
        <HomeFrase
            frase="'Construindo o futuro da web, hoje. Tecnologia de ponta, sites de excelência.'"
        />
        <HomeProjects 
            srcImagem="https://i.ibb.co/gynCSNF/index.png" 
            altImagem="Imagem da tela inicial do projeto Geek OP" 
            srcIconUm="https://i.ibb.co/f27wdz5/spring.png"
            altIconUm="Icone da logo do framework Spring" 
            srcIconDois="https://i.ibb.co/WnqxL8d/html.png"
            altIconDois="Icone da logo do HTML"  
            srcIconTres="https://i.ibb.co/bFXpr1R/css.png"
            altIconTres="Icone da logo do CSS"
            lado="left"
            href="https://vimeo.com/897747118"
        />
        <HomeProjects 
            srcImagem="https://i.ibb.co/MGg05dJ/plat.png" 
            altImagem="Imagem da tela inicial da plataforma EAD" 
            srcIconUm="https://i.ibb.co/HXq4tBM/vue.png"
            altIconUm="Icone da logo do framework Vue Js" 
            srcIconDois="https://i.ibb.co/drrxzN9/laravel.png"
            altIconDois="Icone da logo do framework Laravel"  
            srcIconTres="https://i.ibb.co/wyzL97g/mysql.png"
            altIconTres="Icone da logo do banco de dados MySQL"
            lado="right"
            href="https://vimeo.com/manage/videos/897806834"
        />
        <HomeBtnContact />
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