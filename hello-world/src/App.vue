<template>
<div>
  {{greet}} {{name}}
</div>
<div v-text="position"></div>
  
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      greet: "Hello",
      name: "Fatoom",
      position: "Software Engineer"
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
