<template>
  <!-- Lista con icona, testo ed elementi -->
  <div class="small-list">
    <div class="image"><img src="../../assets/img/24.png" alt="" /></div>
    <div class="text">
      <h3>Online Marketing</h3>
      <p>It is a long estabilished fact that a reader will be distracted.</p>
      <ul>
        <li v-for="(item, i) in listItemsArray" :key="item + i">{{ item }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "SmallList",
  data() {
    return {
      listItemsArray: ["SEO", "SEM", "Website Strategy", "Social management"],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";
.small-list {
  display: flex;
}

.image {
  width: 60px;
  img {
    width: 100%;
  }
}

.text {
  width: 210px;
  margin-left: 25px;
  margin-right: 5px;
  p {
    padding-top: 10px;
    padding-bottom: 15px;
  }
}

ul {
  list-style: none;

  li {
    font-size: 12px;
    margin: 12px 0;
    &::before {
      content: "\f00c";
      padding-right: 10px;

      color: $iconColorSecond;
      font-family: FontAwesome;
      font-size: 10px;
    }
  }
}
</style>
