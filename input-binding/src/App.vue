<template>
  <div id="app">
    <AddBlog />
  </div>
</template>

<script>
import AddBlog from "./components/addBlog.vue";

export default {
  name: "App",
  components: {
    AddBlog,
  },
};
</script>

<style>
body {
  margin: 0;
  font-family: "Nunito SemiBold";
}
</style>
