<template>
  <div>
    <h2>Article Components</h2>
    <h2>{{ title }}</h2>
    <h2>Likes - {{ likes }}</h2>
    <h2>Published - {{ isPublished ? "Yes" : "No" }}</h2>
    <h2 v-bind="$attrs">{{ title }}</h2>
  </div>
</template>

<script>
//31.Prop Types and Validations -
//32.Non-Prop Attributes -

export default {
  name: "PropsValidations",
  props: {
    title: {
      type: String,
      required: true,
      default: 'Article default title'
    },
    likes: Number,
    isPublished: Boolean,
  },
  inheritAttrs: false,
  
  data() {
    return {};
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
