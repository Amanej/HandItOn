<template>
    <footer>
        <!--<p>Here is a footer</p>-->
        <h3>Hand It On 2018</h3>
        <!--
        <h4>Kvalitetsprodukter til gode priser</h4>
        <ul class="row firstRow">
            <li>Alle produkter er kvalitetsikret</li>
            <li>Kjøp brukt raskt, enkelt og trygt</li>
        </ul>
        -->
        <a href="https://amanmender.com">By Aman</a>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    padding: 20px;
    background: white;
    //border-top: 1px solid lightgrey;    
    //margin-top: 20px;
    display: block;
    float: left;
    width: 100%;
    background: #333333;

    h3, h4 {
        font-weight: 400;
    }
    h3 {
        font-weight: 500;

        color: white;
        text-decoration: underline;
    }
    h4 {
        font-style: italic;
        color: white;
    }
    ul.row {
        margin: 10px 0;
        li {
            color: white;
        }
    }
    a {
        color: white;
    }
}
</style>