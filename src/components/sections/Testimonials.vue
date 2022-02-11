<template>
  <!-- Sezione Testimonials -->
  <section>
    <img class="background-waves" src="../../assets/img/15.png" />

    <div class="container">
      <div class="text">
        <h2>Our Testimonials</h2>
        <p>
          If you are planning a product landing app or website, <br />take a
          look at this beautiful-crafted
        </p>
      </div>

      <div class="testimonials">
        <Testimonial
          v-for="(item, i) in testimonialsArray"
          :key="item.name + i"
          :image="item.image"
          :name="item.name"
          :role="item.role"
          :description="item.description"
        />
      </div>

      <div class="dots">
        <span class="dot active"><i class="fa-solid fa-circle"></i></span>
        <span class="dot"><i class="fa-solid fa-circle"></i></span>
      </div>
    </div>
  </section>
</template>

<script>
import Testimonial from "../commons/Testimonial.vue";

export default {
  name: "Testimonials",
  components: {
    Testimonial,
  },
  data() {
    return {
      testimonialsArray: [
        {
          image: "26.jpeg",
          name: "Julia Aann",
          role: "COO Sofbox",
          description:
            "At vero eos et accusamus et iusto odio dignissimos dicimus qui praesentium vero eos et consectetur accus adip adip.",
        },
        {
          image: "27.jpeg",
          name: "Marc Znder",
          role: "Manager Sofbox",
          description:
            "At vero eos et accusamus et iusto odio dignissimos dicimus qui praesentium vero eos et consectetur accus adip adip.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  padding-top: 65px;
  margin-top: 75px;

  background: linear-gradient(
    180deg,
    rgba(239, 245, 255, 1) 0%,
    rgba(0, 212, 255, 0) 100%
  );

  position: relative;
}

.background-waves {
  width: 83%;

  position: absolute;
  top: 0px;
}

.text {
  text-align: center;
  margin-bottom: 80px;

  position: relative;
  z-index: 1;

  h2 {
    margin-bottom: 12px;
  }
}

.testimonials {
  display: flex;
  justify-content: center;
}

.dots {
  margin-top: 30px;
  text-align: center;

  .dot {
    font-size: 7px;
    color: $iconColorMain;

    margin: 0 2px;

    &.active {
      color: $iconColorSecond;
    }
  }
}
</style>
