<template>
  <div id="app">
    <Header :current_question = index />
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="10" offset="1"><Question /></b-col>
      </b-row>
    </b-container>
  </div>
</template>



<script>
import Question from "./components/Question.vue"
import Header from "./components/Header.vue"

export default {
  name: 'App',
  components: {
  Question,
  Header
  },
  data(){
    return{
      
    }
    }
}







</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #067522;
  margin-top: 60px;
}

#bv-example-row{
background-color: transparent;


}

</style>

<style>
body {
  background-image: url("./assets/back.png");
  background-repeat:no-repeat;
  
}
</style>

 