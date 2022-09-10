<template>
  <div id="app">
    <HeaderComponent :title="title"/>
    <NinjasComponent :ninjas="ninjas"/>
    <FooterComponent :title="title"/>
  </div>
</template>

<script>
import FooterComponent from "./components/FooterComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import NinjasComponent from "./components/NinjasComponent.vue";

export default {
  name: "App",
  components: {
    FooterComponent,
    HeaderComponent,
    NinjasComponent,
  },
  data() {
    return {
      ninjas: [
        { name: "Ryu", speciality: "Vue Components", show: false },
        { name: "Crystal", speciality: "HTML Wizardry", show: false },
        { name: "Hitoshi", speciality: "Click Events", show: false },
        { name: "Tango", speciality: "Conditionals", show: false },
        { name: "Kami", speciality: "Webpack", show: false },
        { name: "Yoshi", speciality: "Data Diggin", show: false },
      ],
      title:'Vue Ninjas'
    };
  },
};
</script>

<style></style>
