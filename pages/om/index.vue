<template>
    <div class="om">
        <h1>Hos HandItOn får du tidligere eide kles og elektronikkprodukter fra de beste merkene, i god stand.</h1>
        <!--<div class="cta">
            <h2>Å kjøpe brukt må ikke være vanskelig</h2>
        </div>-->
        <ul>
            <li>
                <p>Å kjøpe brukt må ikke være vanskelig</p>
            </li>
            <li>
                <p>Hjelpe miljøet og spar penger ved å kjøpe brukt</p>
            </li>
            <li>
                <p>Kvalitetsprodukter varer ved ansvarlig bruk</p>
            </li>
        </ul>
        <p class="lastInfo">
            Vi kvalitetsjekker hvert eneste produkt, så du slipper.
        </p>
    </div>
</template>

<style lang="scss" scoped>
div.om {
    padding: 20px;
    width: 80%;
    margin-left: 10%;
    margin-top: 5%;
    h1 {
        text-align: center;
        font-weight: 100;
        padding: 0 20%;
    }
    ul {
        width: 100%;
        padding-left: 0;
        margin: 5% 0;
        li {
            display: inline-block;
            padding: 80px;
            font-size: 24px;
            font-weight: 400;
            width: 100%;
            @media screen and (min-width: 960px) {
                //width: 50%;
            }
            p {
                font-size: 22px;
            }           
            &:first-child {
                background: linear-gradient(to right,#fff, rgba(255, 255, 255, 0.15)), url('~/assets/images/payments/mobile-payments.jpg');
                background-size: cover;
                background-position: center;
                background-attachment: fixed;
            }
            &:nth-child(2) {
                background: linear-gradient(to left,#fff, rgba(255, 255, 255, 0.15)), url('~/assets/images/environments/environment_save_money.jpg');
                background-size: cover;
                background-position: center;
                background-attachment: fixed;
                text-align: right;
            }
            &:nth-child(3) {
                background: linear-gradient(to right,#fff, rgba(255, 255, 255, 0.15)), url('~/assets/images/brands/brands.jpg');
                background-size: cover;
                background-position: center;
                background-attachment: fixed;
            }
        }
    }
    p.lastInfo {
        text-align: center;
        font-size: 24px;
        margin-bottom: 25px;
    }
}
</style>