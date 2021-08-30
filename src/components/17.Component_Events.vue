<template>
  <div>
    <h2>This is a popup</h2>
    <input type="text" v-model="name" />
    <button @click="$emit('close', name)">Close popup</button>
  </div>
</template>

<script>
//34.Component Events -
//35.Validating Emitted Events - 

export default {
  name: "ComponentEvents",
  emits: ['close'],
  /*emits:{
      close: (name) => {
          if(!name) {
              return false
          }
          else {
              return true
          }
      }
  },*/
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
