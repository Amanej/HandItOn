<template>
    <div class="produkt">
        <!--<h1>iPhone X</h1>
        <h2>Apple</h2>-->
        <div class="images">
            <!-- Images -->
            <img v-for="image in images" :src="image.src" :key="image.key" />
        </div>
        <div class="productInfo">
            <h1>iPhone X</h1>
            <h4>Apple</h4>
            <h2>Pris: 9500,-</h2>
            <div class="productSelection">
                <select name="selectColor" class="selectColor">
                    <option disabled default>Velg en farge</option>
                    <option value="stellergrå">Stellargrå</option>
                    <option value="svart">Svart</option>
                </select>
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
                Super Retina HD-skjerm<br/>
                5,8-tommers (diagonalt) OLED Multi‑Touch-skjerm som dekker hele forsiden<br/>
                HDR-skjerm<br/>
                Oppløsning på 2436 x 1125 ved 458 ppi<br/>
                Kontrastforhold på 1 000 000:1 (normal)<br/>
                True Tone-visning<br/>
                Skjerm med stort fargerom (P3)<br/>
                3D Touch<br/>
                625 cd/m2 maksimum lysstyrke (normal)<br/>
                Fingeravtrykk­bestandig, oljeavstøtende belegg<br/>
                Støtte for visning av flere språk og tegnsett samtidig<br/>

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
                //width: 55%;
            }
            div.productSelection {
                padding: 10px;
                select {
                    margin: 5px 5px 5px 0px;
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
            }
        }
    }
}
</style>

<script>
export default {
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