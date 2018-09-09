<template>
<div class="selg">
    <h2>Selg dine high-end brukte ting, uten kjas og mas</h2>
    <p>Å selge sine brukte ting, trenger ikke å innebære masse chatting, pruting og å møte folk når det ikke passer. Simpelthen registrer deg og send oss produktet når det er solgt. </p>
    <h3>Jeg vil selge</h3>
    <p>Klikk på produktet du ønsker å selge via HandItOn</p>
    <!--
    <a href="https://aman305.typeform.com/to/jFD1bh">iPhone X</a>
    <a href="https://aman305.typeform.com/to/jFD1bh">MacBook Pro</a>
    -->

    <!--
    <a href="https://aman305.typeform.com/to/jFD1bh">Samsung Galaxy</a>
    <a href="https://aman305.typeform.com/to/jFD1bh">Louis Vuitton</a>
    <a href="https://aman305.typeform.com/to/jFD1bh">Ganni Kjole</a>
    -->

    <a href="https://aman305.typeform.com/to/jFD1bh" v-for="product in products" :key="product.id">
        <img :src="product.images[0].url" />
        <h4>{{product.name}}</h4>
    </a>
</div>
</template>

<style lang="scss" scoped>
div.selg {
    width: 80%;
    margin-left: 5%;
    padding: 2.5%;
    h2, h3 {
        font-weight: 400;
        text-align: center;
    }
    h3 {
        text-decoration: underline; 
        //margin-bottom: 0;
    }
    p {
        padding: 40px 20%;
        text-align: center;
    }
    a {
        display: inline-block;
        text-align: center;
        width: 25%;
        img {
            width: 100%;
        }
    }
}
</style>

<script>
import products from '@/assets/products.json';

export default {
    asyncData(context) {
        console.log("Products ",products);
        return {
            products: products
        }
    }
}
</script>