<template>
  <section class="container">
    <div class="splash">
      <h1>Hand It On</h1>
      <p>Kjøp og selg <br/> brukte merkevarer</p>
    </div>
    <div class="sellingPoints">
      <div>
        <h2>Kvalitetsprodukter varer</h2>
        <p>Vi overøses i billig varer, men kvalitetsprodukter er de som varer. Når du kjøper de brukt, sparer du lommeboka på langsikt.</p>
      </div>
      <div>
        <h2>Kjøp brukte varer raskt, og enkelt</h2>
        <p>Alle varene blir personlig inspisert, og må ha kvittering i tillegg til å være i god stand. </p>
      </div>
    </div>
    <div class="selection">
      <h2>Utvalg</h2>
      <!-- Products -->
      <!-- Brands -->
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style lang="scss" scoped>
div.splash {
  background: linear-gradient(rgba(83, 83, 83, 0.4),rgba(83, 83, 83, 0.4)),url('~/assets/images/brands/apple/macbook/macbook.jpg') no-repeat center;
  background-size: 80%;
  text-align: center;
  padding: 15%;
  color: white;
  font-family: 'Cambria';

  width: 100%;
  float: left;  
  h1 {
    font-size: 64px; //2em;
  }
  p {
    font-size: 26px; //1.4em;
  }
}
div.sellingPoints {
  width: 100%;
  float: left;
  div {
    background: #6A6969;
    width: 50%;
    display: block;
    float: left;
    color: white;
    text-align: center;
    height: 400px;
    padding: 10% 5%;
    h2 {
      font-weight: 500;
    }
    p {
      padding: 20px 40px;
      font-size: 1.2em;
    }
  }
}
div.selection {
  width: 100%;
  float: left;

  padding: 20px;
  h2 {
    text-align: center;
    font-weight: 500;
  }
}
</style>
