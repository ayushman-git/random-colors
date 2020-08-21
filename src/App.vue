<template>
  <div id="app">
    <random-button v-on:clicked="randomizeColor" :randomColor="randomColor"></random-button>
  </div>
</template>

<script>
import Button from "./components/Button.vue";

export default {
  name: "App",
  data() {
    return {
      randomColor: null,
    };
  },
  components: {
    "random-button": Button,
  },
  methods: {
    randomizeColor() {
      this.randomColor = "#" + Math.random().toString().slice(2, 8);
      console.log(this.randomColor);
    },
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Maven+Pro:wght@900&display=swap');
* {
  box-sizing: border-box;
}

body {
  padding: 0;
  margin: 0;
}

#app {
  display: flex;
  height: 100vh;
  justify-content: center;
  align-items: center;
}
</style>
