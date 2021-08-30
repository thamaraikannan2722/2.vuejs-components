<template>
  <h2>Hello {{ name }} - {{ heroName }}</h2>
</template>

<script>

//30.Component Props - 

export default {
  name: "Components",
  props: ['name', 'heroName'],
  data() {
    return {
    };
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