<template>
    <div class="checkout">
        
        <div class="top">
            <h2>Bestill</h2>
        </div>
        <div class="row">
            <div class="part product">
                <img src="https://tubby.scene7.com/is/image/tubby/APPIPX64BK_2?$fullsize$" />
                <div class="info">
                    <h3>Iphone X</h3>
                    <h4 class="detail"><span class="property">Farge:</span> Sølvgrå</h4>
                    <h4 class="detail"><span class="property">Minne:</span> 64 gb</h4>
                    <h5 class="price"><span class="property">Pris:</span> 7500,-</h5>
                </div>
            </div>
            <div class="part shipment">
                <h3>Forsendelse</h3>
                <input type="text" name="name" class="name" v-model="shipping.name" placeholder="Ditt navn" />
                <input type="text" name="adresse" class="adresse" v-model="shipping.address" placeholder="Adresse" />
                <input type="text" name="postnr" class="postnr" v-model="shipping.postal" placeholder="Postnr" />
                <input type="text" name="sted" class="sted" v-model="shipping.area" placeholder="Sted" />
                <label for="pickup">
                    <input type="checkbox" name="pickup" class="pickup" v-model="shipping.method" id="pickup" />Hent i Oslo Sentrum
                </label>
            </div>
        </div>
        

        <div class="row" v-if="shippingInfoCompleted">
            <div class="part payment">
                <h3>Betal med kort</h3>
                <input type="text" name="kortnummer" class="kortnummer" />
                <input type="text" name="navn" class="navn" />
                <input type="text" name="dato" class="date" />
                <input type="text" name="year" class="year" />
            </div>
            <div class="part finish">
                <h2>Totalt: 7500 kr</h2>
                <button class="complete" @click="completeOrder">Fullfør</button>
            </div>
        </div>
        <div class="assurance">
            <p>Alle våre produkter er personlig inspisert av oss, kommer med original kvittering og garanti.</p>
            <p>
                <strong>Har du noen spørsmål?</strong>
                Da kan du chatte med oss ved å trykke ned i hjørnet.
            </p>
        </div>
        
    </div>
</template>

<script>
export default {
    methods: {
        completeOrder: function() {
            console.log("Complete order");
            // Process payment
            // Send order to API
        }
    },
    computed: {
        shippingInfoCompleted: function() {
            var shipping = this.shipping;
            if(shipping.name && shipping.address && shipping.postal && shipping.area) {
                return true
            }
            return false
        }
    },
    data() {
        return {
            shipping: {
                name: "",
                address: "",
                postal: "",
                area: "",
                method: false
            }
        }
    }
}
</script>

<style lang="scss" scoped>
div.checkout {
    margin: 2% 5%;
    padding: 20px;
    div.top {
        border-bottom: 2px solid #333;
        width: 100%;
        h2 {
            font-weight: 400;
            font-size: 1.8em;
        }
    }
    div.row {
        width: 100%;
        float: left;
    }
    div.part {
        h3 {
            font-weight: 400;
            font-size: 1.2em;
        }
        &.product {
            width: 50%;
            float: left;
            padding: 20px;
            img {
                width: 50%;
                float: left;
                height: auto;
                align-self: center;
                padding: 20px;
                
            }
            div.info {
                //display: flex;
                width: 50%;
                padding-top: 20px;
                float: left;
                h3 {
                    font-weight: 400;
                    font-size: 1.6em;
                }
                h4.detail {
                    color: lighten(#333, 20%);
                    font-weight: 400;
                    font-size: 1.2em;
                    span.property {
                        font-weight: 600;
                    }
                }
                h5.price {
                    font-size: 1.4em;
                    font-weight: 400;
                    margin-top: 20px;
                }
            }
        }
        &.shipment {
            width: 50%;
            float: left;
            padding: 45px;
            input[type="text"] {
                width: 100%;
                font-size: 1em;
                margin: 5px 0;
                padding: 5px;
                &.postnr {
                    width: 30%;
                    margin-right: 5%;
                }
                &.sted {
                    width: 65%;
                }
            }
            label {
                padding-left: 10px;
                line-height: 1.2em;
                margin-top: 15px;
                input[type="checkbox"] {
                    margin-right: 10px;
                }
            }
        }
        &.payment {
            width: 50%;
            float: left;
            padding: 45px;
            input[type="text"] {
                width: 100%;
                font-size: 1em;
                margin: 5px 0;
                padding: 5px;
            }
        }
        &.finish {
            width: 50%;
            float: left;
            padding: 45px;
            text-align: center;
            padding-top: 120px;
            h2 {
                font-weight: 400;
                font-size: 1.2em;
            }
            button {
                font-size: 1.2em;
                background: #13C23F;
                border: none;
                color: white;
                padding: 5px 20px;
                border-radius: 4px;
                margin-top: 10px;
            }
        }
    }
    div.assurance {
        width: 100%;
        float: left;
        padding: 45px;
        text-align: center;
        background: #333;
        color: white;
        p {
            font-size: 1.4em;
            padding: 20px;
            strong {
                display: block;
            }
        }
    }
}
</style>