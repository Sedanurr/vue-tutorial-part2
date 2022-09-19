<template>
  <div>
    <AppHeader />
    <router-view></router-view>
  </div>
</template>

<script>
import AppHeader from "./components/appHeader.vue";

export default {
  components: {
    AppHeader,
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
