<template>
  <!-- Post della sezione Posts -->
  <div class="post">
    <a :href="url">

      <div class="date">{{ date }}</div>
      <div class="image">
        <img :src="require(`../../assets/img/${image}`)" :alt="title" />
      </div>
      
      <div class="text">
        <div class="title">{{ title }}</div>
        <p>{{ paragraph }}</p>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  name: "Post",
  props: {
    url: String,
    date: String,
    image: String,
    title: String,
    paragraph: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

.post {
  width: 270px;
  height: 310px;
  padding: 10px;
  margin: 12px;

  border: 1px solid $borderColorThird;
  border-radius: 4px;

  position: relative;

  .image {
    img {
      width: 100%;
    }
  }

  .text {
    margin-top: 18px;

    .title {
      font-family: $fontMain;
      font-weight: bold;
      font-size: 14px;

      margin-bottom: 10px;
    }
  }

  .date {
    position: absolute;
    top: 18px;
    left: 18px;

    color: $textColorSecond;
    font-size: 11px;

    background-color: $backgroundColorMain;

    padding: 4px 8px;
    border-radius: 4px;
  }
}
</style>
