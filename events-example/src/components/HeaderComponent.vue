<template>
  <header>
    <h1 v-on:click="changeTitle">{{ title }}</h1>
  </header>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
    },
  },
  data() {
    return {
      titlePri: "vue ninja",
    };
  },
  methods: {
    changeTitle: function () {
      this.$emit('changeTitle','Vue Wizards')
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
