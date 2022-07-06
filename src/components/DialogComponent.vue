<template>
  <div>
  </div>
</template>

<script>
export default {
  name: "DialogComponent",
  data() {
    return {
      time: undefined,
    };
  },
  methods: {
    onClose() {
      this.time = Date.now();
      this.$emit("dialog-closed", this.time);
    },
  },
};
</script>

<style></style>
