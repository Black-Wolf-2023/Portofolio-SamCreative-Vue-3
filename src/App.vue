<template>
  <div id="app">
     <header-app></header-app>
     <hero-app></hero-app>
     <!-- <load-view></load-view> -->
  </div>
</template>

<script>
// import LoadView from './components/LoadView.vue';
import HeaderApp from './components/HeaderApp.vue';
import HeroApp from './components/HeroApp.vue';
export default {
  name: 'App',
  components: {
    // LoadView,
    HeaderApp,
    HeroApp
  }
}
</script>

<style lang="scss">
  @import './sass/rest';
  @import './sass/main';
</style>
