<template>
  <div>
    <ShowBlogs />
    <ListBlogs />
  </div>
</template>

<script>
// Imports
import ShowBlogs from "./components/showBlogs.vue";
import ListBlogs from "./components/listBlogs.vue";

export default {
  components: {
    ShowBlogs,
    ListBlogs,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style>
body {
  margin: 0;
  font-family: "Nunito SemiBold";
}
</style>
