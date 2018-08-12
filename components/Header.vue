<template>
    <nav>
        <nuxt-link to="/produkter">Browse</nuxt-link>
        <nuxt-link to="/produkter/kjoler">Kjoler</nuxt-link>
        <nuxt-link to="/produkter/vesker">Vesker</nuxt-link>
        <nuxt-link to="/produkter/mobiler">Mobiler</nuxt-link>
        <nuxt-link to="/produkter/laptop">Laptop</nuxt-link>
        <nuxt-link to="/om">Om</nuxt-link>
    </nav>
</template>

<style lang="scss" scoped>
nav {
    padding: 20px;
    background: #333;
    a {
        color: white;
        margin: 5%;
    }
}
</style>