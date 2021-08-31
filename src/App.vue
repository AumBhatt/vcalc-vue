<template>
  <Display></Display>
  <Keys>{{key}}</Keys>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Keys from './components/Keys.vue'
import Display from './components/DisplayOutput.vue'

export default {
  name: 'App',
  data() {
    return {
      currentExp: '',
      historyList: [
        {id:0, exp: "3"},
        {id:1, exp: "1"},
        {id:2, exp: "2"},
        {id:3, exp: "10"},
        {id:4, exp: "11"},
        {id:5, exp: "2"},
        {id:6, exp: "0"},
        {id:7, exp: "0"},
        {id:8, exp: "0"},
        {id:9, exp: "0"},
        {id:10, exp: "0"},
        {id:11, exp: "0"},
        {id:12, exp: "0"},
        {id:13, exp: "0"},
      ]
    }
  },
  components: {
    Keys, Display
  }
}
</script>

<style>
body {
  background: black;
}
#app {
  width: 100%;
  height: 95vh;

  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  background: green;
}
</style>
