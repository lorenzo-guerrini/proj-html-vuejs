<template>
  <footer>
    <div class="container">
      <div class="info">
        <a href="#"><img src="../../assets/img/35.png" alt="Sofbox" /></a>
        <p>
          It is a long estabilished fact that a reader will be distracted by the
          readable content.
        </p>
        <div>Copyright @2018 <a href="#">Sofbox</a></div>
      </div>
      <div class="footer-links">
        <ul
          v-for="(category, i) in footerItemsArray"
          :key="category.categoryName + i"
        >
          <h4>{{ category.categoryName }}</h4>
          <li
            v-for="(item, i) in category.links"
            :key="category.categoryName + item.name + i"
          >
            <a :href="item.url">{{ item.name }}</a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      footerItemsArray: [
        {
          categoryName: "Menu",
          links: [
            {
              name: "About Us",
              url: "#",
            },
            {
              name: "Theme",
              url: "#",
            },
            {
              name: "Features",
              url: "#",
            },
            {
              name: "Pricing",
              url: "#",
            },
            {
              name: "Blog",
              url: "#",
            },
          ],
        },
        {
          categoryName: "About Us",
          links: [
            {
              name: "About Sofbox",
              url: "#",
            },
            {
              name: "Roadmap",
              url: "#",
            },
            {
              name: "How It Work",
              url: "#",
            },
            {
              name: "Team",
              url: "#",
            },
            {
              name: "News",
              url: "#",
            },
          ],
        },
        {
          categoryName: "Quick Links",
          links: [
            {
              name: "About Us",
              url: "#",
            },
            {
              name: "Theme",
              url: "#",
            },
            {
              name: "Features",
              url: "#",
            },
            {
              name: "Pricing",
              url: "#",
            },
            {
              name: "Blog",
              url: "#",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

footer {
  border-top: 1px solid $borderColorFifth;
}

.container {
  padding: 60px 0;
  display: flex;
}

.info {
  width: 210px;
  margin-right: 25px;
  font-size: 12px;
  color: $textColorSecond;

  img {
    width: 110px;
  }

  p {
    padding-bottom: 40px;
  }

  a {
    color: $textColorThird;
  }
}

.footer-links {
  display: flex;
}

ul {
  list-style: none;

  margin: 0 80px;

  h4 {
    margin-bottom: 20px;
  }
  li {
    font-size: 12px;
    margin-bottom: 12px;
    a {
      color: $textColorSecond;
    }
  }
}
</style>
