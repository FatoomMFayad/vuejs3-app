<template>
  <h2>{{ 2 + 3 + 5}}</h2>
  <h2>{{ 10 + 15 + 5}}</h2>
  <h2>Add method - {{ add(2, 3, 7) }}</h2>
  <h2>Multiply method - {{ multiply(this.baseValue) }}</h2>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      baseMultiplier: 5,
      baseValue: 2
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    multiply(num) {
      return num * this.baseMultiplier;
    }
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
