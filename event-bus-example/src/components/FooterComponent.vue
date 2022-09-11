<template>
  <footer>
    <p>{{ copyright }} {{titleClone}}</p>
  </footer>
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
      copyright: "Copyright 2022",
      titleClone:this.title
    };
  },
  created() {
    bus.$on("titleChanged", (data) => {
      this.titleClone= data;
    });
  },
};
</script>
<style scoped>
footer {
  background: #222;
  padding: 6px;
}
p {
  color: lightgreen;
  text-align: center;
}
</style>
