<template>
  <div id="app">
    
    
    <waifu wf="You got ligma"/>
    <img alt="Vue logo" src={{ZeroTwo.img}}>
  </div>
</template>

<script>

import waifu from './components/Waifu.vue'

export default {
  name: 'App',
  components: {
    waifu
  }
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
  margin-top: 60px;
}
</style>

<style>
body {
  background-image: url("./assets/back.png");
  background-repeat:no-repeat;
}
</style>

 