<template>
    <div class="om">
        <h1>Hos HandItOn får du tidligere eide kles og elektronikkprodukter fra de beste merkene, i god stand.</h1>
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
    </div>
</template>

<style lang="scss" scoped>
div.om {
    padding: 20px;
    h1 {
        text-align: center;
        font-weight: 100;
    }
    ul {
        width: 100%;
        padding-left: 0;
        li {
            display: inline-block;
            padding: 40px;
            font-size: 24px;
            font-weight: 100;
            width: 100%;
            @media screen and (min-width: 960px) {
                width: 50%;
            }
            p {
                font-size: 22px;
            }           
        }
    }
}
</style>