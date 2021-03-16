<template>
  <h2>Volume Tracker (0-20)</h2>
  <h3>Current Volume - {{ volume }}</h3>
  <div>
    <button @click="volume+=2">Increase Volume</button>
    <button @click="volume-=2">Decrease Volume</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      volume: 0
    };
  },
  methods: {
   
  },
  computed: {
    
  },  
  watch:{
    volume(newValue, oldValue) {
      if(newValue > oldValue && newValue === 16) {
        alert('listening to a high volume for a long time may damage your hearing')
      }
    }
  }  
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

label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}
input[type='text'],
textarea,
select{
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
}
</style>
