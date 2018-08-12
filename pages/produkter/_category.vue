<template>
    <div class="produktene">
        <p>Produktene du har valgt {{category}}</p>
        <ul>
            <li v-for="product in products" :key="product.id">
                <img :src="product.images[0].url" />
                <h2>{{product.name}}</h2>
                <h4>Pris: {{product.pris}},-</h4>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
div.produktene {
    padding: 20px;
    text-align: center;
    margin: 20px;    
    p {
        font-size: 24px;
        margin-bottom: 40px;
    }
    ul {
        width: 100%;
        padding-left: 0;
        li {
            width: 50%;
            list-style: none;
            display: inline-block;
            /*height: 600px;
            background-size: cover;
            background-position: center;*/
            img {
                width: 100%;
            }
            h2 {
                text-align: center;
                font-weight: 400;
            }
            h4 {
                font-weight: 400;
            }
        }
    }
}
</style>

<script>
import products from '@/assets/products.json';

//console.log(products);

export default {
    asyncData(context) {
        console.log("Params ",context.params.category);
        var matchedproducts = products.filter(p => p.category === context.params.category);
        return {
            products: matchedproducts,
            category: context.params.category
        }
    }
}
</script>