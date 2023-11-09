<template>
  <HeaderApp />
  <MainContent />
  <NavbarComponent />
</template>

<script>
import HeaderApp from './components/HeaderApp.vue';
import MainContent from './components/MainContent.vue';
import NavbarComponent from './components/NavbarComponent.vue';
  export default {
    components: {
      HeaderApp,
      MainContent,
      NavbarComponent,
    },
    data(){
      return {

      }
    },
  }
</script>

<style lang="scss" >

</style>
