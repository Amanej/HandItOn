<template>
    <div class="produkt">
        <!--<h1>iPhone X</h1>
        <h2>Apple</h2>-->
        <div class="images">
            <!-- Images -->
            <img v-for="(image,index) in product.images" :src="image.url" :key="index" />
        </div>
        <div class="productInfo">
            <h1>{{product.name}}</h1>
            <h4>Apple</h4>
            <h2>Pris: {{product.pris}},-</h2>
            <div class="productSelection">
                <!--<select name="selectColor" class="selectColor">
                    <option disabled default>Velg en farge</option>
                    <option value="stellergrå">Stellargrå</option>
                    <option value="svart">Svart</option>
                </select>-->
                <div class="selector" v-if="product.attributes" v-for="attribute in product.attributes" :key="attribute.name">
                    <label for="">Velg {{attribute.name}}</label>
                    <select :name="attribute.name">
                        <option v-for="val in attribute.values" :key="val">{{val}}</option>
                    </select>
                </div>
                <button class="addToCart">Kjøp nå</button>
            </div>
            <div class="description">
                <!-- Beskrivelse -->
                <!--
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
                    Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
                    Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. 
                    Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                -->
                <h3>Egenskaper</h3>
                <ul>
                    <li>Super Retina HD-skjerm</li>
                    <li>5,8-tommers (diagonalt) OLED Multi‑Touch-skjerm som dekker hele forsiden</li>
                    <li>HDR-skjerm</li>
                    <li>Oppløsning på 2436 x 1125 ved 458 ppi</li>
                    <li>Kontrastforhold på 1 000 000:1 (normal)</li>
                    <li>True Tone-visning</li>
                    <li>Skjerm med stort fargerom (P3)</li>
                    <li>3D Touch</li>
                    <li>625 cd/m2 maksimum lysstyrke (normal)</li>
                    <li>Fingeravtrykk­bestandig, oljeavstøtende belegg</li>
                    <li>Støtte for visning av flere språk og tegnsett samtidig</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
div.produkt {
    padding: 20px;
    //display: flex;
    display: block;
    float: left;
    width: 100%;
    h1,h2 {
        font-weight: 100;
        padding-left: 10px;
    }
    h1 {
        border-bottom: 1px solid #efefef;
    }
    h2 {
        font-weight: 100;
        //padding-left: 20px;
        margin: 10px 0;
    }
    h4 {
        font-size: 14px;
        font-weight: 400;
        font-style: italic;
        padding-left: 20px;        
    }
    div {
        &.images {
            //display: inline-block;
            display: block;
            float: left;
            width: 100%;
            @media only screen and (min-width: 600px) {
                width: 55%;
            }
            img {
                width: 100%;
            }
        }
        &.productInfo {
            //display: inline-block;
            display: block;
            float: left;
            width: 100%;
            @media only screen and (min-width: 600px) {
                width: 40%;

                position: sticky;
                top: 5%;
            }
            div.productSelection {
                padding: 10px;
                padding-top: 0;
                div.selector {
                    padding: 5px 0;
                    label {
                        padding-left: 5px;
                    }
                    select {
                        //font-size: 16px;
                    }
                }
                select {
                    margin: 5px 5px 5px 0px;
                    display: block;
                    min-width: 150px;
                    font-weight: 100;
                    //font-size: 18px;
                }
                button {
                    display: block;
                    margin: 10px;
                    margin-left: 0;
                }
                button.addToCart {
                    background: #333333;
                    color: white;
                    border: none;
                    padding: 6px 10px 7px 10px;
                    font-size: 16px;                    
                }
            }
            div.description {
                padding: 10px;            
                h3 {
                    font-weight: 400;
                    text-decoration: underline;
                }
                ul {
                    padding-left: 0;
                    li {
                        list-style-type: none;
                    }
                }
            }
        }
    }
}
</style>

<script>
import products from '@/assets/products.json';

export default {
    asyncData(context) {
        var product = products.filter(p => p.slug === context.params.slug)[0];
        console.log("Product ",product);
        return {
            product: product
        }
    },
    data: function() {
        return {
            images: [
                {
                    key: 24234234,
                    src: "https://tubby.scene7.com/is/image/tubby/APPIPX64BK_2?$fullsize$"
                }
            ]
        }
    }
}
</script>