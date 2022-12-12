<!-- Importiamo i components -->
<script>
  import Header from './components/Header.vue'
  import MainPage from './components/MainPage.vue'


  export default{
    components:{
      Header,
      MainPage,
    }
  }
</script>

<!-- Diamo una struttura ai components -->
<template>
 <Header />
 <MainPage />
</template>

<!-- Diamo uno stile ai components -->
<style lang="scss" scoped>


</style>
