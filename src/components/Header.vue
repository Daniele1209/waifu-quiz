<template>
   <div>
  <b-nav tabs>
    <b-nav-item disabled><h3><b>Waifu Quiz App</b></h3></b-nav-item>
    <b-nav-item disabled> {{current_question}} </b-nav-item>
  </b-nav>
   </div> 
</template>
<script>
export default {
  props:{
    current_question: Number,
  }

}
</script>