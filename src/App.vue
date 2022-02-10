<template>
  <!-- Macros + BackToTheTop -->
  <div id="app">
    <Header :headerMenuItems="headerArray" :cartCounter="cart" />
    <Main />
    <Footer :footerMenuItems="footerArray" />
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
  data() {
    return {
      headerArray: [
        {
          text: "Home",
          url: "#",
          active: true,
        },
        {
          text: "About us",
          url: "#",
          active: false,
        },
        {
          text: "Feature",
          url: "#",
          active: false,
        },
        {
          text: "Testimonials",
          url: "#",
          active: false,
        },
        {
          text: "Contact US",
          url: "#",
          active: false,
        },
      ],
      cart: 0,
      footerArray: [
        {
          categoryName: "Menu",
          links: [
            {
              name: "About Us",
              url: "#",
            },
            {
              name: "Theme",
              url: "#",
            },
            {
              name: "Features",
              url: "#",
            },
            {
              name: "Pricing",
              url: "#",
            },
            {
              name: "Blog",
              url: "#",
            },
          ],
        },
        {
          categoryName: "About Us",
          links: [
            {
              name: "About Sofbox",
              url: "#",
            },
            {
              name: "Roadmap",
              url: "#",
            },
            {
              name: "How It Work",
              url: "#",
            },
            {
              name: "Team",
              url: "#",
            },
            {
              name: "News",
              url: "#",
            },
          ],
        },
        {
          categoryName: "Quick Links",
          links: [
            {
              name: "About Us",
              url: "#",
            },
            {
              name: "Theme",
              url: "#",
            },
            {
              name: "Features",
              url: "#",
            },
            {
              name: "Pricing",
              url: "#",
            },
            {
              name: "Blog",
              url: "#",
            },
          ],
        },
      ],
    };
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
</style>
