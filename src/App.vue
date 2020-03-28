<template>
  <div id="app">
    
    <img id="waif" src="./assets/zerotwo.jpg"/>
    <waifu wf="You got ligma"/>
    <img name="waifd" src="./assets/zerotwo.jpg"/>

  </div>
</template>

<script>

var ZeroTwo={ 
    name:"Zero Two",
    img:"./assets/nois.png"
}



document.write(ZeroTwo.img);

window.onload = function() {


  
  ZeroTwo.img="./assets/nois.png";
  document.getElementsByName('waifd').src="./assets/nois.png";
};




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

 