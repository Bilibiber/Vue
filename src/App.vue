<template>
  <h1>Hello {{ name }}</h1>
  <h1 v-text="name"></h1>
  <p v-html="htmlBind"></p>
  <button v-bind:disabled="isDisabled">Bind</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Mason",
      htmlBind: "<b>Hello World</b>",
      isDisabled: true
    };
  }
};
</script>

<style>
* {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  top: 0;
  bottom: 0;
}
</style>
