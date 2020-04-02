<template>

<div class="question-box " >
  <b-jumbotron header="Which waifu is this?" class="opacity-2">
    <template v-slot:lead>
      


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
    <br>
  <h4>
    {{index+1}}
  </h4>
  </b-jumbotron>
</div>
</template>
<script>

       
export default {
    props:{
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
            {
            name: "Raphtalia",
            img: require("@/assets/raphtalia.jpg")
            },

            {
            name:"Mai Sakurajima",
            img:require("@/assets/mai.jpg")
            },

            {
            name:"Uraraka",
            img:require("@/assets/uraraka.jpg")
            },
             {
            name:"Chika",
            img:require("@/assets/chika.jpg")
            },
             {
            name:"Rikka Takarada",
            img:require("@/assets/rikka.jpg")
            },
             {
            name:"Rias Gremory",
            img:require("@/assets/rias.jpg")
            },
             {
            name:"Hestia",
            img:require("@/assets/hestia.jpg")
            },
             {
            name:"Ayanami Rei",
            img:require("@/assets/rei.jpg")
            },
             {
            name:"Senjougahara",
            img:require("@/assets/senjougahara.jpg")
            },
             {
            name:"Misaki Mei",
            img:require("@/assets/misaki.jpg")
            },
             {
            name:"Sinon",
            img:require("@/assets/sinon.jpg")
            },
             {
            name:"Speedwagon",
            img:require("@/assets/speedwagon.jpg")
            },
             {
            name:"Esdeath",
            img:require("@/assets/esdeath.jpg")
            },
             {
            name:"Makise Kurisu",
            img:require("@/assets/makise.jpg")
            },
             {
            name:"Megumin",
            img:require("@/assets/megumin.jpg")
            },
             {
            name:"Mari Ohara",
            img:require("@/assets/mari.jpg")
            },
             {
            name:"Rui Tachibana",
            img:require("@/assets/rui.jpg")
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
color: #08a823c7;
background-color:transparent;
opacity: 0.2;
}
</style>