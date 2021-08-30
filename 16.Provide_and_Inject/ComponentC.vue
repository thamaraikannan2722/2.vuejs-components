<template>
  <h2>Component C</h2>

  <ComponentE />
</template>

<script>

//33.Provide and Inject - 

import ComponentE from '../16.Provide_and_Inject/ComponentE';

export default {
  name: "ComponentC",
  components: {
      ComponentE,
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