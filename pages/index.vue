<template>
    <Head>
        <Title>GPS.ev - {{ name }}</Title>
    </Head>
    <header>
        <HomeNavbar />
    </header>
    <main>
        <HomeSlogan />
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