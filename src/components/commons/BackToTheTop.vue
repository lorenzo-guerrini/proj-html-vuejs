<template>
  <!-- Pulsante che se cliccato manda a inizio pagina -->
  <div id="back-to-top">
    <a href="#"><i class="fa-solid fa-chevron-up"></i></a>
  </div>
</template>

<script>
export default {
  name: "BackToTheTop",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

#back-to-top {
  position: fixed;
  bottom: 30px;
  right: 17px;
  z-index: 999;

  a {
    background-color: $backgroundColorFifth;
    color: $textColorFourth;

    padding: 9px 13px 8px 13px;
    border-radius: 50%;
  }
}
</style>
