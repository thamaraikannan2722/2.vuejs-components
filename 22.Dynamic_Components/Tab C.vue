<template>
  <div>Tab C Component</div>
  <input type="text" v-model="name">
</template>

<script>

//41.Dynamic_Components - 

export default {
  name: "TabC",
  data() {
    return {
        name: '',
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