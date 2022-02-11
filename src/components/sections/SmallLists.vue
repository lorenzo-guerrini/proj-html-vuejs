<template>
  <!-- Sezione SmallLists -->
  <section>
    <div class="container">
      <SmallList
        v-for="(item, i) in listsArray"
        :key="item.title + i"
        :image="item.image"
        :title="item.title"
        :paragraph="item.paragraph"
        :listItemsArray="item.arrayItems"
      />
    </div>
  </section>
</template>

<script>
import SmallList from "../commons/SmallList.vue";
export default {
  name: "SmallLists",
  components: {
    SmallList,
  },
  data() {
    return {
      listsArray: [
        {
          image: "24.png",
          title: "Online Marketing",
          paragraph:
            "It is a long estabilished fact that a reader will be distracted.",
          arrayItems: ["SEO", "SEM", "Website Strategy", "Social management"],
        },
        {
          image: "24.png",
          title: "Online Marketing",
          paragraph:
            "It is a long estabilished fact that a reader will be distracted.",
          arrayItems: ["SEO", "SEM", "Website Strategy", "Social management"],
        },
        {
          image: "24.png",
          title: "Online Marketing",
          paragraph:
            "It is a long estabilished fact that a reader will be distracted.",
          arrayItems: ["SEO", "SEM", "Website Strategy", "Social management"],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  margin-top: 100px;
}

.container {
  display: flex;
}
</style>
