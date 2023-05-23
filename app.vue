<template>
  <div>
    <Header ref="header" />
    <main class="main-section">
      <NuxtPage />
    </main>
    <CallToAction />
    <Footer />
  </div>
</template>

<script>
  export default {
    name: 'MainApp',
    methods:{
      scrollEvent(){

        this.$refs.header.scrollAnimation() ;
      }
    },
    mounted(){
      
        window.addEventListener('scroll', this.scrollEvent)
    }
  }
</script>

<style lang="scss">
  *{
    margin: 0px ;
    padding: 0px ;

    --font-family: 'Roboto', sans-serif ;
  }
  html, body, .main-section{
    width: 100% ;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
  .main-wrapper{
    width: 100% ;
    display: flex ;
    flex-direction: column;
  }

  a.router-link-active{
    text-decoration: none;
  }
</style>
