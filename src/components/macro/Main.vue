<template>
  <!-- Commons: SmallList -->
  <!-- Sections: Jumbotron, TextAndImage, Features, Testimonials, Posts, Contact -->
  <main>
    <Jumbotron
      :title="'The biggest platform for your growth.'"
      :paragraph="'There are many variations of passages of Lorem Ipsum aviable, but the majority have suffered alteration in some form'"
      :buttonLink="'#'"
      :image="'27-1.png'"
    />
  </main>
</template>

<script>
import Jumbotron from "../sections/Jumbotron.vue";

export default {
  name: "Main",
  components: {
    Jumbotron,
  },
};
</script>

<style></style>
