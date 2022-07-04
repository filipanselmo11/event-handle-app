<template>
  <div>
    <child-component @user-chosen="updateUser"></child-component>
  </div>
</template>

<script>
import ChildComponent from "./ChildComponent.vue";

export default {
  name: "ParentComponent",
  components: {
    ChildComponent,
  },
  data: () => ({}),
  methods: {
    updateUser(user) {
      console.log(user.name, user.username);
    },
  },
};
</script>

<style></style>
