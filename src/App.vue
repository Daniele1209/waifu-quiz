<template>
  <div id="app">
    <Header />

    <b-container class = "bv-example-row">
      <b-row>
        <b-col sm = "6" offset = "3">
          <Questions
            :current_question = 'questions[index]'
            :next = 'next'
            :input = "input"
            :answer = "questions[index].answer"
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
          answer: "Rem",
          url : require("@/assets/rem.jpg")
        },
        {
          answer: "Zero Two",
          url: require("@/assets/zerotwo.png")
        },
        {
          answer: "Midnight",
          url: require("@/assets/midnight.jpg")
        },
        {
          answer: "Raphtalia",
          url: require("@/assets/raphtalia.jpg")
        },
        {
          answer: "Mai Sakurajima",
          url: require("@/assets/mai.jpg")
        },
        {
          answer: "Uraraka",
          url: require("@/assets/uraraka.jpg")
        },
        {
          answer: "Chika",
          url: require("@/assets/chika.jpg")
        },
        {
          answer: "Rikka Takarada",
          url: require("@/assets/rikka.jpg")
        },
        {
          answer: "Rias Gremory",
          url: require("@/assets/rias.jpg")
        },
        {
          answer: "Hestia",
          url: require("@/assets/hestia.jpg")
        },
        {
          answer: "Ayanami Rei",
          url: require("@/assets/rei.jpg")
        },
        {
          answer: "Senjougahara",
          url: require("@/assets/senjougahara.jpg")
        },
        {
          answer: "Misaki Mei",
          url: require("@/assets/misaki.jpg")
        },
        {
          answer: "Sinon",
          url: require("@/assets/sinon.jpg")
        },
        {
          answer: "Speedwagon",
          url: require("@/assets/speedwagon.jpg")
        },
        {
          answer: "Esdeath",
          url: require("@/assets/esdeath.jpg")
        },
        {
          answer: "Makise Kurisu",
          url: require("@/assets/makise.jpg")
        },
        {
          answer: "Megumin",
          url: require("@/assets/megumin.jpg")
        },
        {
          answer: "Mari Ohara",
          url: require("@/assets/mari.jpg")
        },
        {
          answer: "Rui Tachibana",
          url: require("@/assets/rui.jpg")
        }

      ],
      index: 0,
      input: ""
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
  body {
    background-image: url("./assets/back.gif");
    background-repeat: no-repeat;
    background-size:cover;
  }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f1f6ff;
  margin-top: 50px;
}
</style>
