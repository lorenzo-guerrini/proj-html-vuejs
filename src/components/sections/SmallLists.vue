<template>
  <section>
    <div class="container">
      <SmallList />
      <SmallList />
      <SmallList />
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
};
</script>

<style lang="scss" scoped>
section {
  padding: 100px 0;
}
.container {
  display: flex;
}
</style>
