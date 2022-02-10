<template>
  <div class="card" :class="{ active: isActive }">
    <div class="image">
      <img :src="require(`../../assets/img/${image}`)" :alt="title" />
    </div>
    <div class="text">
      <div class="title">{{ title }}</div>
      <p>{{ paragraph }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    isActive: Boolean,
    image: String,
    title: String,
    paragraph: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

.card {
  display: flex;

  padding: 25px 8px 25px 10px;

  cursor: pointer;

  &.active {
    border: 1px solid $borderColorSecond;
    box-shadow: 5px 35px 30px 0px #f0f0f0;

    position: relative;
    z-index: 1;

    .title {
      color: $textColorThird;
    }
  }
}

.image {
  width: 110px;

  display: flex;
  align-items: center;
  img {
    width: 100%;
  }
}

.text {
  margin-left: 15px;
  .title {
    font-family: $fontMain;
    font-size: 14px;
    font-weight: bold;

    margin-bottom: 10px;
  }
}
</style>
