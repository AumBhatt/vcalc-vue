<template>
  <Keys>{{key}}</Keys>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Keys from './components/Keys.vue'

export default {
  name: 'App',
  components: {
    Keys
  }
}
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
