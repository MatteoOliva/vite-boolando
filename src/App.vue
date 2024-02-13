<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppCard from './components/AppCard.vue';
import {store} from './store'




export default {
  data() {
    return {
      store: store,
      products: []
    };
  },

  components: { AppHeader, AppMain, AppFooter, AppCard },

  created() {
    axios.get('http://localhost:3000/products').then((res) => {
      this.products = res.data;
});
  },
};

</script>

<template>
  
  <AppHeader></AppHeader>
  <AppMain :products="products"></AppMain>
  <AppFooter></AppFooter>
  <AppCard></AppCard>
  
</template>

<style lang="scss">
@use './styles/general.scss';
</style>
