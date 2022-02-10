<template>
  <!-- Sections: TextAndImage, Features, Testimonials, Posts, Contact -->
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
  </main>
</template>

<script>
import Jumbotron from "../sections/Jumbotron.vue";
import SmallLists from "../sections/SmallLists.vue";
import TextAndImage from "../sections/TextAndImage.vue";
import Features from "../sections/Features.vue";

export default {
  name: "Main",
  components: {
    Jumbotron,
    SmallLists,
    TextAndImage,
    Features,
  },
};
</script>

<style>
main {
  padding-top: 62px;
}
</style>
