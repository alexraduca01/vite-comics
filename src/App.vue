<template>
  <HeaderApp />
  <MainContent />
  <NavbarComponent />
  <FooterApp />
</template>

<script>
import HeaderApp from './components/HeaderApp.vue';
import MainContent from './components/MainContent.vue';
import NavbarComponent from './components/NavbarComponent.vue';
import FooterApp from './components/FooterApp.vue';
  export default {
    components: {
      HeaderApp,
      MainContent,
      NavbarComponent,
      FooterApp,
    },
    data(){
      return {

      }
    },
  }
</script>

<style lang="scss" >

</style>
