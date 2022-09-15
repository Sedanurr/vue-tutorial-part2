<template>
  <div>
      <HeaderComponent />
      <router-view></router-view>
  </div>
</template>

<script>

import HeaderComponent from './components/headerComponent.vue';

export default {
  components: {
    HeaderComponent
},
  data () {
      return {

      }
  },
  methods: {

  }
}
</script>

<style>
body{
  margin: 0;
  font-family: 'Nunito SemiBold';
}
</style>