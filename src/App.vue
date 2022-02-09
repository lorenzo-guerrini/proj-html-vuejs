<template>
  <!-- Macros + BackToTheTop -->
  <div id="app">
    <Header />
    <Main />
    <Footer />
    <BackToTheTop />
  </div>
</template>

<script>
import Header from "@/components/macro/Header.vue";
import Main from "@/components/macro/Main.vue";
import Footer from "@/components/macro/Footer.vue";
import BackToTheTop from "@/components/commons/BackToTheTop.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
    BackToTheTop,
  },
};
</script>

<style lang="scss">
@import "./assets/style/global.scss";
@import "./assets/style/vars.scss";

@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");
@font-face {
  font-family: "now-light";
  src: local("now-light"), url("./assets/fonts/now-light.otf");
}

body {
  font-family: "Poppins", sans-serif;
  h2 {
    font-family: $fontMain;
  }
}
</style>
