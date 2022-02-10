<template>
  <!-- No commons, no sections -->
  <header>
    <div class="container">
      <div class="logo">
        <a href="#"><img src="../../assets/img/logo-2.png" alt="Sofbox" /></a>
      </div>

      <nav>
        <ul>
          <li
            v-for="(item, i) in headerMenuItems"
            :key="item.text + i"
            :class="{ active: item.active }"
          >
            <a :href="item.url">{{ item.text }}</a>
          </li>
        </ul>

        <div class="icons">
          <div class="search">
            <i class="fa-solid fa-magnifying-glass"></i>
          </div>
          <div class="cart">
            <i class="fa-solid fa-cart-shopping"></i>
            <div class="cart-counter">
              <span>{{ cartCounter }}</span>
            </div>
          </div>
        </div>

        <a href="" class="button">Get Started</a>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    headerMenuItems: Array,
    cartCounter: Number,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

header {
  font-family: $fontMain;
  font-size: 12px;
  font-weight: bold;

  background-color: $backgroundColorMain;

  width: 100%;

  position: fixed;
  z-index: 999;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;

  padding: 5px 0;
}

.logo {
  width: 35px;
  img {
    width: 100%;
  }
}

nav {
  display: flex;
  margin-right: 80px;

  color: $textColorMain;

  ul {
    display: flex;

    list-style-type: none;

    li {
      display: flex;
      align-items: center;

      margin: 0 10px;
      padding-bottom: 5px;

      &.active {
        border-bottom: 1.5px solid $borderColorMain;

        a {
          color: $backgroundColorThird;
        }
      }
    }
  }

  .icons {
    margin: 0 30px;
    display: flex;
    align-items: center;

    div {
      margin: 0 10px;
    }
  }

  a.button {
    font-size: 10.5px;
    font-weight: bold;
  }
}

.cart {
  position: relative;

  .cart-counter {
    position: absolute;
    top: -7px;
    left: -1px;

    font-size: 8px;

    background-color: $backgroundColorThird;
    color: $textColorFourth;

    padding: 4px 5px 2px 5px;
    border-radius: 50%;

    text-align: center;
    z-index: -1;
  }
}
</style>
