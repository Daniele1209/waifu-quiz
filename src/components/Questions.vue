<template>
    <div class = "question_box" >
        <b-jumbotron style="background-color: rgba(245, 245, 245, 0.2); ">
            <template v-slot:lead>
                <b-img v-bind:src = "current_question.url" alt=""
                     height = "300px"
                     weight = "300px"
                ></b-img>

            </template>
            <hr class = "my-6" />
            <p>
                <b>Enter name here :</b>
            </p>
            <p>
                <input v-model = "input" @keyup.enter = "check_name"/>
            </p>
            <b-button v-model = "input" variant="success" @click = "check_name" >Next</b-button>
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
        methods: {
            check_name() {
                if (this.input === this.answer)
                    this.next();
                 else
                    return false;
            }
        }
    }

</script>

<style>
    #question_box {
        background: linear-gradient(to right, rgba(226,226,226,1) 0%, rgba(254,254,254,1) 100%);
    }

</style>
