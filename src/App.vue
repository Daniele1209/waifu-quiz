<template>
  <div id="app">
    <Header />

    <b-container class = "bv-example-row">
      <b-row>
        <b-col sm = "6" offset = "3">
          <Questions
            :current_question = 'questions[index]'
            :next = 'next'
          />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Questions from "./components/Questions.vue"

export default {
  name: 'App',
  components: {
    Header,
    Questions
  },
  data() {
    return {
      questions: [
        {
          answer: "Zero two",
          url : require("@/assets/zerotwo.png")
        },
        {
          answer: "Midnight",
          url: require("@/assets/midnight.jpg")
        },
        {
          answer: "Rem",
          url: require("@/assets/rem.jpg")
        }
      ],
      index: 0
    }
  },
  methods: {
    next() {
      this.index++
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
  color: #2c3e50;
  margin-top: 50px;
}
</style>
