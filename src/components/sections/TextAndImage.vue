<template>
  <!-- Sezione TextAndImage -->
  <section>
    <div class="container">
      <div class="text">
        <h2>Get tips tricks on how to skyrocket your sales.</h2>
        <p>
          Faff about only a quid blower I don’t want no agro bleeding chimney
          pot burke tosser cras nice one boot fanny!
        </p>

        <Card
          v-for="(item, i) in cardsArray"
          :key="item.title + i"
          :id="item.id"
          :isActive="selected == item.id ? true : false"
          :image="item.image"
          :title="item.title"
          :paragraph="item.paragraph"
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
      cardsArray: [
        {
          id: 0,
          image: "510.png",
          title: "Reporting Analysis",
          paragraph:
            "It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.",
        },
        {
          id: 1,
          image: "511.png",
          title: "Technical SEO Audit",
          paragraph:
            "It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  padding-top: 100px;
}

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
