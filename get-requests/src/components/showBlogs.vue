<template>
  <div id="show-blogs">
    <h1>All Blog Articles</h1>
    <div v-for="(blog, index) in blogs" :key="index" class="single-blog">
      <h2>{{ blog.title }}</h2>
      <article>{{ blog.body }}</article>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      blogs: [],
    };
  },
  methods: {},
  created() {
    this.$http
      .get("http://jsonplaceholder.typicode.com/posts")
      .then((response) => {
        this.blogs = response.body.slice(0, 10);
      });
  },
};
</script>
<style>
    #show-blogs{
        max-width:800px;
        margin:0 auto;
    }
    .single-blog{
        padding:20px;
        box-sizing: border-box;
        margin:20px 0;
        background: #eee;
    }
</style>
