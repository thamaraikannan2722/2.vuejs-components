<template>
  <div>
    <h4>ChildStyles component text</h4>
  </div>
</template>

<script>
//40.Component Styles -

export default {
  name: "ComponentStyles",
  data() {
    return {};
  },
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h4 {
    color: olivedrab;
}
</style>
