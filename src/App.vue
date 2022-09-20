<template>
  <div id="app">
     <HeaderApp/>
      <hero-app></hero-app>
      <div class="break"></div>
      <offer-app></offer-app>
      <div class="break"></div>
      <details-app></details-app>
      <project-app></project-app>
      <icons-app></icons-app>
      <tools-app></tools-app>
     <FooterApp/>
     <!-- <load-view></load-view> -->
  </div>
</template>

<script>
// import LoadView from './components/LoadView.vue';
import HeaderApp from './components/HeaderApp.vue';
import HeroApp from './components/HeroApp.vue';
import OfferApp from './components/OfferApp.vue';
import DetailsApp from './components/DetailsApp.vue';
import ProjectApp from './components/ProjectApp.vue';
import IconsApp from './components/IconsApp.vue';
import ToolsApp from './components/ToolsApp.vue';
import FooterApp from './components/FooterApp.vue';
export default {
  name: 'App',
  components: {
    // LoadView,
    HeaderApp,
    HeroApp,
    OfferApp,
    DetailsApp,
    ProjectApp,
    IconsApp,
    ToolsApp,
    FooterApp
  }
}
</script>

<style lang="scss">
  @import './sass/rest';
  @import './sass/main';
</style>
