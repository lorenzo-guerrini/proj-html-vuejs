<template>
  <!-- Sezione Features -->
  <section>
    <div class="container">
      
      <div class="text">
        <div>
          <h2>Popular features that your business needs</h2>
          <p>
            Faff about only a quid blower I don’t want no agro bleeding chimney
            pot burke tosser cras nice one boot fanny.!
          </p>
        </div>
        <a href="#" class="button">Explore More Feature</a>
      </div>

      <div class="features">
        <Feature
          v-for="(item, i) in featuresArray"
          :key="item.name + i"
          :name="item.name"
          :icon="item.icon"
          :color="item.color"
        />
      </div>
    </div>

    <img class="background-circle" src="../../assets/img/14.png" />
  </section>
</template>

<script>
import Feature from "../commons/Feature.vue";

export default {
  name: "Features",
  components: {
    Feature,
  },
  data() {
    return {
      featuresArray: [
        {
          name: "Customized Invoices",
          icon: "fa-solid fa-chart-line",
          color: "blue",
        },
        {
          name: "Stock Management",
          icon: "fa-solid fa-paper-plane",
          color: "red",
        },
        {
          name: "Receivable & Payables",
          icon: "fa-solid fa-award",
          color: "green",
        },
        {
          name: "Manage buying",
          icon: "fa-solid fa-face-smile",
          color: "blue",
        },
        {
          name: "Powerful & Secure",
          icon: "fa-solid fa-virus-covid",
          color: "red",
        },
        {
          name: "Fastest Return Filing",
          icon: "fa-solid fa-award",
          color: "green",
        },
        {
          name: "Monthly Detailed",
          icon: "fa-solid fa-pen-to-square",
          color: "blue",
        },
        {
          name: "Product Management",
          icon: "fa-solid fa-thumbs-up",
          color: "red",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  margin-top: 90px;
  position: relative;
}

.text {
  display: flex;
  align-items: center;
  justify-content: space-between;

  h2 {
    margin-bottom: 12px;
  }

  p {
    display: inline-block;
    width: 420px;

    margin-bottom: 15px;
  }

  .button {
    font-size: 12px;
    margin-right: 65px;
  }
}

.features {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}

.background-circle {
  width: 500px;

  position: absolute;
  z-index: -2;
  top: -75px;
  left: -360px;
}
</style>
