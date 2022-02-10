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
  </main>
</template>

<script>
import Jumbotron from "../sections/Jumbotron.vue";
import SmallLists from "../sections/SmallLists.vue";
import TextAndImage from "../sections/TextAndImage.vue";

export default {
  name: "Main",
  components: {
    Jumbotron,
    SmallLists,
    TextAndImage,
  },
};
</script>

<style>
main {
  padding-top: 62px;
}
</style>
