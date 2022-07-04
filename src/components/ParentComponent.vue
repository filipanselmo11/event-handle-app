<template>
  <div :style="{ background: backgroundColor }">
    <child-component @color-chosen="colorChosen"></child-component>
  </div>
</template>

<script>
import ChildComponent from "./ChildComponent.vue";

export default {
  name: "ParentComponent",
  components: {
    ChildComponent,
  },
  data: () => ({
    backgroundColor: "",
  }),
  methods: {
    colorChosen(color) {
      this.backgroundColor = color;
      console.log("BACKGROUND -> ", this.backgroundColor);
    },
  },
};
</script>

<style></style>
