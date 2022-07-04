<template>
  <div id="databinding">
    <button @click="displayNumbers">Clik Me</button>
    <h2>Add Number 100 + 200 = {{ total }}</h2>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data: () => ({
    num1: 100,
    num2: 200,
    total: "",
  }),
  methods: {
    displayNumbers(e) {
      console.log(e);
      return (this.total = this.num1 + this.num2);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
