<script>


export default {
  data() {
    return {
      
    };
  },

  props: {
    products: Array
  },


  methods: {
    buildImagePath(imageName) {
        return new URL('../assets/img/' + imageName, import.meta.url).href;
    },

    division(a, b) {
     const quotient = a / b;
     
     return quotient.toFixed(2)
    },
  },

};
</script>

<template>
<main>
    <div class="container">
      <div class="card" v-for="(product, index) in products">
        <img :src="buildImagePath(product.frontImage)" class="front-img" alt="foto-modello" />
        <img :src="buildImagePath(product.backImage)" class="back-img" alt="foto-modello" />       
        <div class="wishlist">
          <i class="fa-solid fa-heart"></i>
        </div>
        <div class="img-content">
          <span class="red-fontt" v-show="product.badges[1].value === '-50%' " > &nbsp; {{ product.badges[1].value}} &nbsp; </span>  
          <span class="red-fontt" v-show="product.badges[0].value === '-30%' " > &nbsp; {{ product.badges[0].value}} &nbsp; </span>        
          <span class="green-font" v-show="product.badges[0].value === 'Sostenibilità' "> &nbsp; {{ product.badges[0].value}} &nbsp;</span>
        </div>

        <div class="descrizione">
          <p>{{product.brand}}</p>
          <h3>{{ product.name }}</h3>
          <p>
            <span class="red-font">{{ product.price }}</span>
            &nbsp;
            <span style="text-decoration: line-through" v-show="product.badges[1].value === '-50%' " > {{ division(product.price, 0.5) }}</span>
            <span style="text-decoration: line-through" v-show="product.badges[0].value === '-30%' " > {{ division(product.price, 0.7) }}</span>
          </p>
        </div>
      </div>
    </div>
  </main>

</template>

<style lang="scss" scoped>

</style>
