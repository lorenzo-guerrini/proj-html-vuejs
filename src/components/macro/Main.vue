<template>
  <main>
    <Jumbotron
      :title="'The biggest platform for your growth.'"
      :paragraph="'There are many variations of passages of Lorem Ipsum aviable, but the majority have suffered alteration in some form'"
      :buttonLink="'#'"
      :image="'27-1.png'"
    />
    <SmallLists />
    <TextAndImage />
    <Features />
    <Testimonials />
    <Posts />
  </main>
</template>

<script>
import Jumbotron from "../sections/Jumbotron.vue";
import SmallLists from "../sections/SmallLists.vue";
import TextAndImage from "../sections/TextAndImage.vue";
import Features from "../sections/Features.vue";
import Testimonials from "../sections/Testimonials.vue";
import Posts from "../sections/Posts.vue";

export default {
  name: "Main",
  components: {
    Jumbotron,
    SmallLists,
    TextAndImage,
    Features,
    Testimonials,
    Posts,
  },
};
</script>

<style>
main {
  padding-top: 62px;
}
</style>
