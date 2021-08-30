<template>
  <h2>Component F</h2>
  <h2>Component F username - {{ username }}</h2>
</template>

<script>

//33.Provide and Inject - 

export default {
  name: "ComponentF",
  data() {
    return {
    };
  },
  inject: ['username'],
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