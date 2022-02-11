<template>
  <!-- Testimonal della sezione Testimonials -->
  <!-- TODO: Immagine, nome, testo -->
  <div class="testimonial">
    <div class="image">
      <img :src="require(`../../assets/img/${image}`)" :alt="name" />
    </div>
    <div class="info">
      <span class="name">{{ name }}</span
      ><span class="role"> - {{ role }}</span>
    </div>
    <p>{{ description }}</p>
  </div>
</template>

<script>
export default {
  name: "Testimonial",
  props: {
    image: String,
    name: String,
    role: String,
    description: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

.testimonial {
  width: 390px;
  height: 260px;
  background-color: $backgroundColorMain;

  padding: 35px 24px;
  border-radius: 4px;

  box-shadow: -6px 15px 30px 0px #f2f2f2;

  display: flex;
  flex-direction: column;
  align-items: center;

  position: relative;

  &::before {
    content: "";
    position: absolute;
    bottom: -9px;
    width: 350px;
    z-index: -1;
    border-radius: 4px;
    height: 100%;
    background-color: $backgroundColorMain;
    box-shadow: -6px 15px 30px 0px #d6d6d6;
  }

  &::after {
    content: "";
    position: absolute;
    bottom: -19px;
    width: 320px;
    left: 0;
    margin: 0 auto;
    right: 0;
    z-index: -2;
    border-radius: 4px;
    height: 100%;
    background-color: $backgroundColorMain;
    box-shadow: -6px 15px 30px 0px #c5c5c5;
  }
}

.image {
  width: 50px;
  margin-bottom: 22px;

  img {
    width: 100%;
    overflow: hidden;

    border: 2px solid $borderColorSixth;
    border-radius: 50%;

    box-shadow: 0px 8px 38px 0px #f3f3f3;
  }
}

.info {
  margin-bottom: 22px;

  .name {
    font-size: 14px;
    font-family: $fontMain;
    font-weight: bold;
  }

  .role {
    color: $textColorSecond;
    font-size: 12px;
    line-height: 22px;
  }
}
</style>
