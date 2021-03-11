<template>
<div>
  {{greet}} {{name}}
</div>
<div v-html="position"></div>
  
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      greet: "Hello",
      name: "Fatoom",
      position: "<b>Software Engineer</b>"
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
