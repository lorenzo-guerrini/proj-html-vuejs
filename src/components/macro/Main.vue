<template>
  <!-- Commons: SmallList -->
  <!-- Sections: Jumbotron, TextAndImage, Features, Testimonials, Posts, Contact -->
  <main>
    <Jumbotron />
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
