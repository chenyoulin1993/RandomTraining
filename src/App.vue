<template>
  <div id="app">
    <Cheast />
  </div>
</template>

<script>

import Cheast from  './components/Cheast'
export default {
  name: 'app',
  components: {
    Cheast
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
