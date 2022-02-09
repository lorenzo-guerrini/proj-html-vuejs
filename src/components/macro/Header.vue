<template>
  <!-- No commons, no sections -->
  <header>
    <div class="container">
      <div class="logo">
        <img src="../../assets/img/logo-2.png" alt="Sofbox" />
      </div>

      <nav>
        <ul>
          <li v-for="(item, i) in menuItems" :key="item.text + i" :class="{'active' : item.active}">
            <a :href="item.url">{{ item.text }}</a>
          </li>
        </ul>

        <div class="icons">
          <div class="search">
            <i class="fa-solid fa-magnifying-glass"></i>
          </div>
          <div class="cart">
            <i class="fa-solid fa-cart-shopping"></i>
          </div>
        </div>

        <button>Get Started</button>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      menuItems: [
        {
          text: "Home",
          url: "#",
          active: true,
        },
        {
          text: "About us",
          url: "#",
          active: false,
        },
        {
          text: "Feature",
          url: "#",
          active: false,
        },
        {
          text: "Testimonials",
          url: "#",
          active: false,
        },
        {
          text: "Contact US",
          url: "#",
          active: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

header {
  font-family: $fontMain;
  font-size: 12px;
  font-weight: bold;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;

  width: 950px;
  margin: auto;
  padding: 10px 0;
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

  button {
    font-size: 10.5px;
    font-weight: bold;
  }
}
</style>
