<template>
  <div id="app">

    <Header/>
    <Main/>
    <PreFooter/>
    <Footer/> 

  </div>
</template>


<script>

  import Header from "./components/Header.vue";
  import Main from "./components/Main.vue";
  import PreFooter from "./components/PreFooter.vue";
  import Footer from "./components/Footer.vue";

  export default {
    name: "App",
    components: {
      Header,
      Main,
      PreFooter,
      Footer,
    },
  };
</script>


<style lang="scss">

  @import "./style/general.scss";
  @import "./style/utilities.scss";

  main{
    height: 100px;
    background-color: black;
    font-family: Open Sans Condensed;
    color: white;
    font-size: 30px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

</style>
