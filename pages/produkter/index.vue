<template>
    <div class="produktene">
        <h2>Velg produktkategori</h2>
        <ul>
            <li v-for="category in categories.categories" :key="category.id">
                <nuxt-link :to="'produkter/'+category.name">
                    <img :src="category.image" />
                    <p>{{category.displayName}}</p>
                </nuxt-link>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
div.produktene {
    padding: 20px;
    text-align: center;
    margin: 20px;    
    h2 {
        text-align: center;
        font-weight: 100;
    }
    ul {
        width: 100%;
        padding-left: 0;
        li {
            display: inline-block;
            width: 50%;
            padding: 40px;
            font-size: 24px;
            font-weight: 100;
            img {
                width: 100%;
            }   
            a {
                color: #333;
                transition: 1s;
                text-decoration: none;
                font-weight: 400;
                &:hover {
                    color: #888;
                    border-color: #888;
                    p {
                        border-color: #888;
                    }
                }
                &:active {
                    color: #555;
                }
                p {
                    display: inline;
                    border-bottom: 1px solid #333;
                    transition: 1s;
                    &:hover {
                        border-color: #888;
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
    computed: {
        categories: function() {
            return {
                categories: [
                    {
                        name: "laptop",
                        displayName: "Laptop",
                        id: 9302,
                        image: "https://tubby.scene7.com/is/image/tubby/MACBPMPTR2HA?$fullsize$"
                    },
                    {
                        name: "mobiler",
                        displayName: "Mobiler",
                        id: 9312,
                        image: "https://tubby.scene7.com/is/image/tubby/APPIPX64BK_2?$fullsize$"
                    },
                    {
                        name: "kjoler",
                        displayName: "Kjoler",
                        id: 9332,
                        image: "https://www.ganni.com/dw/image/v2/AAWT_PRD/on/demandware.static/-/Sites-ganni-master-catalogue/default/dw7ad1958f/images/images/hi-res/F2472-415-1.jpg?sh=2000"
                    },
                    {
                        name: "vesker",
                        displayName: "Vesker",
                        id: 9342,
                        image: "https://uk.louisvuitton.com/images/is/image/lv/1/PP_VP_L/louis-vuitton-pochette-metis-monogram-canvas-handbags--M40780_PM2_Front view.jpg"
                    }
                ]
            }
        }
    }
}
</script>