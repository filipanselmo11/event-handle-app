<template>
  <div>
    <label>My Custom Input</label>
    <input type="text" placeholder="Custom Input" @input="handleChange" />
  </div>
</template>

<script>
export default {
  name: "MyTextInput",
  methods: {
    handleChange(e) {
      this.$emit("custom-change", e.target.value.toUpperCase());
    },
  },
};
</script>

<style scoped></style>
