<template>
  <div id="app">
    <Header />
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="10" offset="1"><Question :current_question= Waifus[index] /></b-col>
      </b-row>
    </b-container>
    
    
    

  </div>
</template>



<script>
import Header from "./components/Header.vue"
import Question from "./components/Question.vue"

export default {
  name: 'App',
  components: {
  Header,
  Question
  },
  data(){
    return{
      Waifus:[
            {
            name: "Rem",
            img: require("@/assets/rem.jpg")
            },

            {
            name:"Zero Two",
            img:require("@/assets/zerotwo.jpg")
            },

            {
            name:"Midnight",
            img:require("@/assets/midnight.jpg")
            },
            
        ],
        index:0
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

 