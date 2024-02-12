<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppCard from './components/AppCard.vue';



export default {
  data() {
    return {
      title:'La Molisana',
    };
  },

  components: { AppHeader, AppFooter, AppCard },
};

</script>

<template>
  
  <AppHeader></AppHeader>
  <AppFooter></AppFooter>
  <AppCard></AppCard>
  
</template>

<style lang="scss">
@use './styles/general.scss';
</style>
