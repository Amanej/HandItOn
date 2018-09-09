<template>
    <nav>
        <!-- Logo -->
        <!--<nuxt-link to="/produkter">Browse</nuxt-link>-->
        <!--<nuxt-link to="/produkter/kjoler">Kjoler</nuxt-link>
        <nuxt-link to="/produkter/vesker">Vesker</nuxt-link>-->
        <div class="produkter">
            <nuxt-link to="/produkter/mobiler">Mobiler</nuxt-link>
            <nuxt-link to="/produkter/laptop">Laptop</nuxt-link>
        </div>
        <div class="om">
            <nuxt-link to="/om">Om</nuxt-link>
            <nuxt-link to="/selg">Selg</nuxt-link>
        </div>
    </nav>
</template>

<style lang="scss" scoped>
nav {
    padding: 20px;
    background: #333;
    a {
        color: white;
        margin: 5% 15%;
    }
    div {
        display: inline-block;
        &.produkter {
            margin-left: 5%;
        }
        &.om {
            float: right;
            margin-right: 5%;
        }
    }
}
</style>