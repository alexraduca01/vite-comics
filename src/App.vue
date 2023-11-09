<template>
  <HeaderApp />
  <MainContent />
</template>

<script>
import MainContent from './components/MainContent.vue';
import HeaderApp from './components/HeaderApp.vue';
  export default {
    components: {
      HeaderApp,
      MainContent,
    },
    data(){
      return {

      }
    },
  }
</script>

<style lang="scss" >

</style>
