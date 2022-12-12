<!-- Importiamo i components -->
<script>
  import Header from './components/Header.vue'
  import MainPage from './components/MainPage.vue'
  import PreFooter from './components/PreFooter.vue'


  export default{
    components:{
      Header,
      MainPage,
      PreFooter,
    }
  }
</script>

<!-- Diamo una struttura ai components -->
<template>
 <Header/>
 <MainPage/>
 <PreFooter/>
</template>

<!-- Diamo uno stile ai components -->
<style lang="scss" scoped>


</style>
