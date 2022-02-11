<template>
  <!-- Sezione Posts -->
  <section>
    <div class="container">
      <h2>Latest Posts</h2>
      <p>If you are planning on developing a product loading.</p>

      <div class="posts">
        <Post
          v-for="(item, i) in postsArray"
          :key="i"
          :url="item.url"
          :date="item.date"
          :title="item.title"
          :image="item.image"
          :paragraph="item.paragraph"
        />
      </div>
    </div>
  </section>
</template>

<script>
import Post from "../commons/Post.vue";

export default {
  name: "Posts",
  components: {
    Post,
  },
  data() {
    return {
      postsArray: [
        {
          url: "#",
          date: "November 28, 2019",
          image: "19.jpg",
          title: "Life Lack Meaning",
          paragraph:
            "It's a long estabilished fact that a reader will be distracted by the readable.",
        },
        {
          url: "#",
          date: "November 28, 2019",
          image: "18.jpg",
          title: "Life Lack Meaning",
          paragraph:
            "It's a long estabilished fact that a reader will be distracted by the readable.",
        },
        {
          url: "#",
          date: "November 28, 2019",
          image: "17.jpg",
          title: "Life Lack Meaning",
          paragraph:
            "It's a long estabilished fact that a reader will be distracted by the readable.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  padding-top: 90px;
}
.container {
  text-align: center;

  h2 {
    margin-bottom: 10px;
  }
}

.posts {
  margin-top: 70px;

  display: flex;
  justify-content: center;
}
</style>
