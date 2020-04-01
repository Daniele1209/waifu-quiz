<template>
    <div class = "question_box">
        <b-jumbotron>
            <img : src = "require(current_question.url)" >


            <hr class = "my-4" />
            <p>
                answer
            </p>

            <b-button variant="success" href="#">Next</b-button>

        </b-jumbotron>
    </div>
</template>


<script>
    export default {
        props: {
            current_question: Object
        }
    }
</script>
