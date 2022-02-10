<template>
  <footer>
    <div class="container">
      <div class="info"></div>
      <div class="footer-links">
        <ul v-for="(category, i) in footerItemsArray" :key="category.categoryName+i">
          <h4>{{category.categoryName}}</h4>
          <li v-for="(item, i) in category.links" :key="category.categoryName+item.name+i">
            <a :href="item.url">{{item.name}}</a>
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


ul {
  list-style: none;
  li a{
    color: $textColorSecond;
  }
}
</style>
