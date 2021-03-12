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
<h2 v-show="display">Using v-show</h2>
<h2 v-for="(name, index) in names" :key="name">{{index}} {{ name }}</h2>
<h2 v-for="name in fullNames" :key="name.first">{{ name.first}} {{name.last}}</h2>
<div v-for="actor in actors" :key="actor.name">
  <h2>{{actor.name}}</h2> 
  <ul v-for="movie in actor.movies" :key="movie">
    <li>{{ movie}}</li>
  </ul>
</div>
<h2 v-for="(value, key) in myInfo" :key="value"> {{key}} {{ value }}</h2>


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
      display: true,
      names:['Fatoom', 'Hanan', 'Mohammed'],
      fullNames:[
        {first: 'Fatoom', last: 'Fayad'},
        {first: 'Hanan', last: 'Fayad'},
        {first: 'Mohammed', last: 'Fayad'},
      ],
      actors:[
        {
          name: 'Christian Bale',
          movies: ['Batman', 'The Prestige']
        },
        {
          name: 'Johny Depp',
          movies: ['Pirates of the Carrebian', 'The Tourist']
        }
      ],
      myInfo:{
        name: 'Fatoom',
        job: 'Software Engineer'
      }
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
