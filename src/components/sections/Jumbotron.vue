<template>
  <!-- Jumbotron con testo e immagine -->
  <section>
    <div class="jumbotron">
      <div class="text">
        <h1>The biggest platform for your growth.</h1>
        <p>
          There are many variations of passages of Lorem Ipsum aviable, but the
          majority have suffered alteration in some form
        </p>
        <button>Read More</button>
      </div>

      <div class="image">
        <img src="../../assets/img/27-1.png" alt="jumbotron" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Jumbotron",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

.jumbotron {
  max-width: 1115px;
  margin: auto;
  padding: 10px 15px;

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

  button {
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
