<template>

<div class="question-box">
  <b-jumbotron header="Which waifu is this?">
    <template v-slot:lead>
        <Waifus :current-question="Waifus" />


      <!--  <div v-for="waifu in Waifus" v-bind:key="waifu"> 
        <img alt="Wf" v-bind:src=waifu.img />
        </div> -->

        <img v-bind:src="Waifus[index].img" alt="lmao" height="400px" width="400px" />

    </template>

    <hr class="my-4">

    <input  />
    <br/>
    <br/>
    <b-button variant="primary" v-on:click="nextWaifu" >Next</b-button>

  </b-jumbotron>
</div>
</template>

<script>

       

export default {
    props:{
        currentquestion: Object
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
  },
  methods:{ 
     nextWaifu(){
         this.index++;
     }
  }    
}


</script>





<style>

#question-box{
color:#08a823c7;
background-color:transparent;
opacity: 0.2;
}
</style>