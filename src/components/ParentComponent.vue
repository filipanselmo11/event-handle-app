<template>
  <div>
    <child-component @changeMsg="setMessage" :msg="welcomeMsg"></child-component>
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
    welcomeMsg: 'Hello World',
  }),
  methods: {
    setMessage(msg){
        this.welcomeMsg = msg;
        console.log('WELCOME MESG -> ', this.welcomeMsg);
    }
    // colorChosen(color) {
    //   this.backgroundColor = color;
    //   console.log("BACKGROUND -> ", this.backgroundColor);
    // },
  },
};
</script>

<style></style>
