<template>
  <section>
    <div class="jumbotron">
      <div class="text">
        <h1>{{ title }}</h1>
        <p>
          {{ paragraph }}
        </p>
        <a class="button" :href="buttonLink">Read More</a>
      </div>

      <div class="image">
        <img :src="require(`../../assets/img/${image}`)" alt="jumbotron" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Jumbotron",
  props: {
    title: String,
    paragraph: String,
    buttonLink: String,
    image: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  padding-bottom: 35px;
}

.jumbotron {
  max-width: 1115px;
  margin: auto;
  padding: 10px 15px;
  border-radius: 8px;

  display: flex;

  background-color: $backgroundColorSecond;
}

.text {
  padding: 35px;
  width: 42%;

  p {
    margin-top: 10px;
    margin-bottom: 45px;
  }

  a.button {
    font-size: 12px;

    margin-bottom: 35px;
  }
}

.image {
  width: 58%;
  padding-top: 5px;

  position: relative;

  img {
    width: 91%;
    right: 20px;
    position: absolute;
  }
}
</style>
