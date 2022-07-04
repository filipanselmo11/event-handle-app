<template>
  <div v-bind:style="{ 'font-family': font }">
    <child-component 
        v-for="(index,post) in posts"
        :key="index"
        @change-font="changeFont"></child-component>
  </div>
</template>

<script>
import ChildComponent from "./ChildComponent.vue";

export default {
  name: "ParentComponent",
  components:{
    ChildComponent
  },
  data: () => ({
    font: "",
  }),
};
</script>

<style></style>
