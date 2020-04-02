<template>
    <div class = "question_box" >
        <b-jumbotron style="background-color: rgba(245, 245, 245, 0.2); ">
            <template v-slot:lead>
                <b-img v-bind:src = "current_question.url" alt="" thumbnail id = "image"></b-img>
            </template>
            <p id = "enter">
                <b id = "text">Guess the waifu :</b>
            </p>
            <p>
                <b-form-input
                        v-model = "input"
                        @keyup.enter = "check_name"
                        :state = "this.ok"
                >
                </b-form-input>
            </p>
            <b-button size = "lg" v-model = "input" variant="info" @click = "check_name">Next</b-button>
        </b-jumbotron>
    </div>
</template>


<script>
    export default {
        props: {
            current_question: Object,
            next: Function,
            input: String,
            answer: String
        },
        data() {
            return {
                ok: null
            }
        },
        methods: {
            check_name() {
                if (this.input === this.answer) {
                    this.ok = null;
                    this.next();
                }
                else {
                    this.ok = false;
                    return false;
                }
            }
        }
    }

</script>

<style>
    #image {
        width: 500px;
        height: 500px;
    }
    #text {
        -webkit-text-stroke: 1.7px black;
    }
    #enter {
        display: inline;
        position: relative;
        font-family: 'Source Sans Pro', sans-serif;
        font-size:40px;
        letter-spacing: -2.3px;
        color: rgba(174, 183, 255, 0.7);
    }
</style>
