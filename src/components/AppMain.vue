<script>
export default {
  data() {
    return {
      products: [
        {
          id: 1,
          frontImage: "1.webp",
          backImage: "1b.webp",
          brand: "Levi's",
          name: "Relaxed Fit",
          price: 29.99,
          isInFavorites: true,
          badges: [
            {
              type: "tag",
              value: "Sostenibilità",
            },
            {
              type: "discount",
              value: "-50%",
            },
          ],
        },
        {
          id: 2,
          frontImage: "2.webp",
          backImage: "2b.webp",
          brand: "Guess",
          name: "Roses Tee",
          price: 20.99,
          isInFavorites: true,
          badges: [
            {
              type: "discount",
              value: "-30%",
            },
            {
              type: "",
              value: "",
            },
          ],
        },
        {
          id: 3,
          frontImage: "3.webp",
          backImage: "3b.webp",
          brand: "Come Zucchero Filato",
          name: "Voglia di colori pastello",
          price: 129.99,
          isInFavorites: false,
          badges: [
            {
              type: "discount",
              value: "-30%",
            },
            {
              type: "",
              value: "",
            },
          ],
        },
        {
          id: 4,
          frontImage: "4.webp",
          backImage: "4b.webp",
          brand: "Levi's",
          name: "Tee Unisex",
          price: 14.99,
          isInFavorites: false,
          badges: [
            {
              type: "tag",
              value: "Sostenibilità",
            },
            {
              type: "discount",
              value: "-50%",
            },
          ],
        },
        {
          id: 5,
          frontImage: "5.webp",
          backImage: "5b.webp",
          brand: "Maya Deluxe",
          name: "Stripe Bodice",
          price: 99.99,
          isInFavorites: true,
          badges: [
            {
              type: "tag",
              value: "Sostenibilità",
            },
            {
              type: "discount",
              value: "-50%",
            },
          ],
        },
        {
          id: 6,
          frontImage: "6.webp",
          backImage: "6b.webp",
          brand: "Esprit",
          name: "Maglione - Black",
          price: 29.99,
          isInFavorites: true,
          badges: [
            {
              type: "tag",
              value: "Sostenibilità",
            },
            {
              type: "",
              value: "",
            },
          ],
        },
      ],
    };
  },

  methods: {
    buildImagePath(imageName) {
        return new URL('../assets/img/' + imageName, import.meta.url).href;
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
          <p>Levi's</p>
          <h3>RELAXED FIT TEE UNISEX</h3>
          <p>
            <span class="red-font">{{ product.price }}</span>
            &nbsp;
            <span style="text-decoration: line-through">29,99€</span>
          </p>
        </div>
      </div>
    </div>
  </main>

</template>

<style lang="scss" scoped>

</style>
