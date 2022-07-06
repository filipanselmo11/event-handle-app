<template>
  <div>
    <my-text-input @custom-change="handleCustomChange"></my-text-input>
  </div>
</template>

<script>
import MyTextInput from './MyTextInput.vue';
export default {
  components: { MyTextInput },
  name: 'ParentComponent',
  data() {
    return {
      uppercase: ''
    }
  },
  methods:{
    handleCustomChange(s){
      this.uppercase = s;
    }
  },
};
</script>

<style></style>
