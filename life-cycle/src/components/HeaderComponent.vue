<template>
  <header>
    <h1 v-on:click="changeTitle">{{ titleClone }}</h1>
  </header>
</template>
<script>
import { bus } from "../main";
export default {
  props: {
    title: {
      type: String,
    },
  },
  data() {
    return {
      titlePri: "vue ninja",
      titleClone: this.title,
    };
  },
  methods: {
    changeTitle: function () {
      // this.$emit("changeTitle", "Vue Wizards");
      this.titleClone = "Vue Wizards";
      bus.$emit("titleChanged", "Vue Wizards");
    },
  },
};
</script>
<style scoped>
header {
  background: lightgreen;
  padding: 10px;
}
h1 {
  text-align: center;
  color: #222;
}
</style>
