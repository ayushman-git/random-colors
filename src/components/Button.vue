<template>
  <button @click="$emit('clicked')" :style="{'background-color': randomColor}">Randomize
    <p>{{ randomColor }}</p>
  </button>
</template>

<script>
export default {
  name: "Button",

  props: {
    randomColor: {
      type: String,
    },
  },
};
</script>

<style scoped>
button {
  font-family: 'Maven Pro', sans-serif;
  color: white;
  font-size: 3em;
  width: 7em;
  height: 7em;
  border-radius: 50%;
  border: none;
  box-shadow: 0px 0px 41px -1px rgba(0,0,0,0.49);
  transition: box-shadow 0.2s linear;
  mix-blend-mode: difference;
}

button:hover {
  box-shadow: 0px 0px 57px 2px rgba(0,0,0,0.72);
}

button:focus {
  outline: none;
}

p {
  font-size: 14px;
}
</style>