<template>
  <div id="databinding">
    <div v-bind:style="styleobj" v-on:mouseover="changebgcolor" v-on:mouseout="originalcolor"></div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data: () => ({
    styleobj: {
      width: "100px",
      height: "100px",
      backgroundColor: "red",
    },
  }),
  methods: {
    changebgcolor() {
      this.styleobj.backgroundColor = "green";
    },
    originalcolor() {
      this.styleobj.backgroundColor = "red";
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
