<template>
  <h2>Component E</h2>

  <ComponentF />
</template>

<script>

//33.Provide and Inject -  

import ComponentF from '../16.Provide_and_Inject/ComponentF';

export default {
  name: "ComponentE",
  components: {
      ComponentF,
  },
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