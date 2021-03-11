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
<h2 v-bind:class="{
  promoted: isPromoted,
  new: !isSoldOut,
  'sold-out': isSoldOut
}">Object Conditional Movie</h2>
<h2 v-bind:style="{
  color: highlightColor,
  'font-size': headerSize + 'px'
}">Inline Style</h2>
<h2 v-bind:style="headerStyle">Style Object</h2>
<h2 v-if="num === 0">The number is zero</h2>
<h2 v-else-if="num < 0">The number is Negative</h2>
<h2 v-else-if="num > 0">The number is Positive</h2>
<h2 v-else>Not a number</h2>

<template v-if="display">
  <h2>Fatoom</h2>
  <h2>SWE</h2>
  <h2>Full Stack</h2>
</template>

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
      isSoldOut: true,
      highlightColor: "orange",
      headerSize: 50,
      headerStyle:{
        color: "orange",
        fontSize: '50px',
        padding: '20px'
      },
      num: "5nnn",
      display: true
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
