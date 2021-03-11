<template>
<div>
  {{greet}} {{name}}
</div>
<div v-html="position"></div>
<h2 v-bind:id="headingId">Heading</h2>
<button v-bind:disabled="isDisabled">Bind</button> 
<h2 class="underline">Underlined Text</h2>
<h2 v-bind:class="status">Status</h2>
<h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
<h2 v-bind:class="isSoldOut? 'sold-out' : 'new'">Sold out Movie</h2>
<h2 v-bind:class="[isPromoted && 'promoted', isSoldOut? 'sold-out' : 'new']">Array conditional Movie</h2>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      greet: "Hello",
      name: "Fatoom",
      position: "<b>Software Engineer</b>",
      headingId: "heading",
      isDisabled: false,
      status: "success",
      isPromoted: true,
      isSoldOut: true
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
.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new{
  color: olivedrab;
}

.sold-out {
  color: red;
}
</style>
