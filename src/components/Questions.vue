<template>
    <div class = "question_box">
        <b-jumbotron>
            <template v-slot:lead>
                <img v-bind:src = "current_question.url" alt = "pic"/>
            </template>
            <hr class = "my-4" />
            <p>
                answer
            </p>

            <b-button variant="success" v-on:click = "next" >Next</b-button>
        </b-jumbotron>
    </div>
</template>


<script>
    export default {
        props: {
            current_question: Object,
            next: Function
        }
    }
</script>
