<template>
  <!-- Sezione SmallLists -->
  <section>
    <div class="container">
      <SmallList
        :image="'24.png'"
        :title="'Online Marketing'"
        :paragraph="'It is a long estabilished fact that a reader will be distracted.'"
        :listItemsArray="arrayItems"
      />
      <SmallList
        :image="'24.png'"
        :title="'Online Marketing'"
        :paragraph="'It is a long estabilished fact that a reader will be distracted.'"
        :listItemsArray="arrayItems"
      />
      <SmallList
        :image="'24.png'"
        :title="'Online Marketing'"
        :paragraph="'It is a long estabilished fact that a reader will be distracted.'"
        :listItemsArray="arrayItems"
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
      arrayItems: ["SEO", "SEM", "Website Strategy", "Social management"],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  margin: 100px 0;
}

.container {
  display: flex;
}
</style>
