<template>
  <div>
    <h2>{{post.title}}</h2>
    <div>{{post.content}}</div>
    <button @click="$emit('change-font')">
        Change Font
    </button>
  </div>
</template>

<script>
export default {
  name: "ChildComponent",
  props: ["post"],
  data: () => ({
    posts: [
      {
        title: "Foo",
        content: "foo",
      },
      {
        title: "Bar",
        content: "bar",
      },
    ],
    font: "",
  }),
  methods: {
    changeFont() {
        this.font === '' ? 'courier' : '';
    },
  },
};
</script>

<style></style>
