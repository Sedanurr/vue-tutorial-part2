<template>
  <div id="app">
    <FormHelper>
      <div slot="form-header">
        <h3>This is the title of the form</h3>
        <p>Information about the form</p>
      </div>
      <div slot="form-fields">
        <input type="text" placeholder="name" required />
        <input type="password" placeholde="password" required>
      </div>
      <div slot="form-controls">
        <button v-on:click="handleSubmit">Submit</button>
      </div>
    </FormHelper>
  </div>
</template>

<script>
import FormHelper from "./components/formHelper.vue";
export default {
  name: "App",
  components: {
    FormHelper,
  },

  data() {
    return {
      title: "I am a dynamic slot title",
    };
  },
};
</script>

<style></style>
