<template>
  <div class="center">
    <h1>Hello {{ name }}</h1>
    <h1 v-text="name"></h1>
    <p v-html="htmlBind"></p>
    <button v-bind:disabled="isDisabled">Bind</button>
    <p v-bind:class="className">This is a underline text</p>
    <h2 v-bind:class="isPromoted && 'promoted'">Joker</h2>
    <h2 v-bind:class="isSoldOut ? 'soldOut' : 'newMovie'">The Avengers</h2>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Mason",
      htmlBind: "<b>Hello World</b>",
      isDisabled: true,
      className: "underline",
      isPromoted: true,
      isSoldOut: true
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
.underline {
  text-decoration: underline;
}
.center {
  display: grid;
  place-items: center;
}

.promoted {
  font-style: italic;
}

.newMovie {
  color: greenyellow;
}

.soldOut {
  color: red;
}
</style>
