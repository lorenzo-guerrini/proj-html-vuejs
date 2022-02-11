<template>
  <!-- Feature della sezione Features -->
  <div class="feature" :class="color">
    <div class="name">{{ name }}</div>
    <div class="icon"><i :class="icon"></i></div>
  </div>
</template>

<script>
export default {
  name: "Feature",
  props: {
    name: String,
    icon: String,
    color: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

.feature {
  width: 200px;
  height: 120px;
  padding: 18px 15px;
  margin-top: 22px;

  background-color: $backgroundColorMain;

  border-radius: 2px;
  box-shadow: 0px 0px 50px 0px #f2f2f2;

  .name {
    font-family: $fontMain;
    font-size: 14px;
    font-weight: bold;
    color: $backgroundColorFourth;

    margin-bottom: 10px;
  }

  .icon {
    font-size: 35px;
  }

  &:hover {
    position: relative;
    z-index: 1;

    .name {
      color: $backgroundColorMain;
    }

    .icon {
      color: $backgroundColorMain !important;
    }
  }

  &.blue {
    .icon {
      color: $iconColorSecond;
    }

    &:hover {
      background-color: $iconColorSecond;
      box-shadow: 0px 0px 50px 0px $iconColorSecond;
    }
  }

  &.red {
    .icon {
      color: $iconsColorThird;
    }

    &:hover {
      background-color: $iconsColorThird;
      box-shadow: 0px 0px 50px 0px $iconsColorThird;
    }
  }

  &.green {
    .icon {
      color: $iconsColorFourth;
    }

    &:hover {
      background-color: $iconsColorFourth;
      box-shadow: 0px 0px 50px 0px $iconsColorFourth;
    }
  }
}
</style>
