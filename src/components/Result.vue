<script setup>
    import { RouterLink } from "vue-router";

    const { numberOfCorrectAnswers, quizQuestionLength } = defineProps({
        numberOfCorrectAnswers: Number,
        quizQuestionLength: Number
    });
</script>

<template>
    <div class="results">
        <p>Your Results...</p>
        <h1>
            {{ numberOfCorrectAnswers }}/{{ quizQuestionLength }}
        </h1>
        <RouterLink to="/">Go Back</RouterLink>
    </div>
</template>

<style scoped>
    .results {
        text-align: center;
        padding: 100px 0;
    }

    p {
        font-size: 25px;
    }

    h1 {
        font-size: 25px;
    }
</style>