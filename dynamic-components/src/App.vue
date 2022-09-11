<template>
  <div id="app">
    <keep-alive> <component v-bind:is="component"></component></keep-alive>
    <button v-on:click="component = 'FormOne'">Show form one</button>
    <button v-on:click="component = 'FormTwo'">Show form two</button>
  </div>
</template>

<script>
import FormOne from "./components/formOne.vue";
import FormTwo from "./components/formTwo.vue";
export default {
  name: "App",
  components: {
    FormOne,
    FormTwo,
  },

  data() {
    return {
      component: "FormOne",
    };
  },
};
</script>

<style></style>
