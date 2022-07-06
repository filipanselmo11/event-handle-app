<template>
  <div>
    <dialog-component @dialog-closed="eventHandler"></dialog-component>
  </div>
</template>

<script>
import DialogComponent from "./DialogComponent.vue";

export default {
  components: { DialogComponent },
  name: "MainComponent",
  methods: {
    eventHandler(e, time) {
      console.log(`Dialog was closed at ${time}`);
    },
  },
};
</script>

<style></style>
