<!-- Importiamo i components -->
<script>
  import Header from './components/Header.vue'
  import MainPage from './components/MainPage.vue'
  import PreFooter from './components/PreFooter.vue'
  import Footer from './components/Footer.vue'


  export default{
    components:{
      Header,
      MainPage,
      PreFooter,
      Footer,
    },
    
  }
</script>

<!-- Diamo una struttura ai components -->
<template>
 <Header />
 <MainPage/>
 <PreFooter/>
 <Footer/>
</template>

<!-- Diamo uno stile ai components -->
<style lang="scss">
  @use './styles/general.scss' as *;


</style>
