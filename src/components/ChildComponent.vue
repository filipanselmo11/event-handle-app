<template>
  <div>
    <button @click="chooseColor('peachpuff')">Peach Puff</button>
    <button @click="chooseColor('skyblue')">Sky Blue</button>
    <button @click="chooseColor('salmon')">Salmon</button>
  </div>
</template>

<script>
export default {
  name: "ChildComponent",
  methods: {
    chooseColor(color) {
      this.$emit("color-chosen", color);
      console.log('COLOR -> ', color);
    },
  },
};
</script>

<style></style>
