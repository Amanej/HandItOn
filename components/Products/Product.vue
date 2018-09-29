<template>
    <nuxt-link :key="product.id" :to="'/produkt/'+product.slug">
        <img :src="product.images[0].url" />
        <h2>{{product.name}}</h2>
        <h4>Pris: {{product.pris}},-</h4>
    </nuxt-link>
</template>

<script>
export default {
    props: {
        Product: Object
    }
}
</script>