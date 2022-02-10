<template>
  <div class="card" :class="{ active: isActive }">
    <div class="image"><img src="../../assets/img/510.png" alt="" /></div>
    <div class="text">
      <div class="title">Reporting Analysis</div>
      <p>
        It is a long established fact that a reader will be distracted by the
        readable content of a page when looking at its layout.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    isActive: Boolean,
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
    box-shadow: 4.871px 34.659px 30px 0px #f0f0f0;

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
