<template>
  <!-- Testo, 2 card (commons), immagine -->
  <section>
    <div class="container">
      <div class="text">
        <h2>Get tips tricks on how to skyrocket your sales.</h2>
        <p>
          Faff about only a quid blower I don’t want no agro bleeding chimney
          pot burke tosser cras nice one boot fanny!
        </p>
        <Card
          id="0"
          :isActive="selected == 0 ? true : false"
          :image="'510.png'"
          :title="'Reporting Analysis'"
          :paragraph="'It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.'"
        />
        <Card
          id="1"
          :isActive="selected == 1 ? true : false"
          :image="'511.png'"
          :title="'Technical SEO Audit'"
          :paragraph="'It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.'"
        />
      </div>
      <div class="image">
        <img src="../../assets/img/509.jpeg" alt="" />
      </div>
    </div>
  </section>
</template>

<script>
import Card from "../commons/Card.vue";

export default {
  name: "TextAndImage",
  components: {
    Card,
  },
  data() {
    return {
      selected: 0,
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
}

.text {
  width: 46%;

  h2 {
    margin-bottom: 10px;
  }

  p {
    margin-bottom: 35px;
  }
}

.image {
  width: 45%;
  margin-left: 20px;

  display: flex;
  align-items: center;
  img {
    width: 100%;
  }
}
</style>
