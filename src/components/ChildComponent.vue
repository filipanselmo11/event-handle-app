<template>
  <div>
    <button @click="chooseUser({ name: 'chris', username: 'chrisoncode' })">
      Choose Chris
    </button>
    <button @click="chooseUser({ name: 'kapehe', username: 'kapehe_ok' })">
      Choose Kapehe
    </button>
  </div>
</template>

<script>
export default {
  name: "ChildComponent",
  methods: {
    chooseUser(user) {
      this.$emit("user-chosen", user);
      console.log('USer -> ', user);
    },
  },
};
</script>

<style></style>
