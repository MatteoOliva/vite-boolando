<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppFooter from './components/AppCard.vue';



export default {
  data() {
    return {
      title:'La Molisana',
    };
  },

  components: { AppHeader, AppMain, AppFooter, AppCard },
};

</script>

<template>
  
  <AppHeader></AppHeader>
  <AppMain></AppMain>
  <AppFooter></AppFooter>
  <AppCard></AppCard>
  
</template>

<style lang="scss">
@use './styles/general.scss';
</style>
