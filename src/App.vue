<!-- src/views/Home.vue -->
<template>
  <div class="wrapper">
    <h1>Flashcards App</h1>
    <FlashcardsList :cards="cards" />
  </div>
</template>

<script setup lang="ts">
import FlashcardsList from "@/components/FlashcardsList.vue";

export default {
  components: {
    FlashcardsList,
  },
  data() {
    return {
      cards: [
        {
          question: "ReactJS",
          answer:
            "This is a JavaScript (user-interface framework) library developed by engineers at Facebook.",
        },
        {
          question: "JSX",
          answer:
            "This is an HTML-like syntax extension for JavaScript written to be used with React. This is specifically how React adds XML syntax to JavaScript which is compiled to JavaScript at runtime.",
        },
        {
          question: "JSX element",
          answer:
            "A basic unit of JSX found in a JavaScript file which is treated as, and has the functionality of, a JavaScript expression. It can also have attributes, just like HTML elements.",
        },
        {
          question: "If a JSX expression takes up more than one line",
          answer: "you must wrap the multi-line expression in parentheses.",
        },
        {
          question: "ReactDOM",
          answer:
            "This is a JavaScript library that contains several React-specific methods, all of which deal with the DOM in some way or another.",
        },
        {
          question:
            "Can component names start with a lowercase letter and why or why not?",
          answer:
            "No. Always start component names with a capital letter. React treats components starting with lowercase letters as DOM tags.",
        },
      ],
    };
  },
};
</script>

<style scoped>
.wrapper {
  font-family: "Roboto";
  text-align: center;
  background-color: #659dbd;
  padding: 20px;
  border-radius: 10px;
}

h1 {
  color: #fff;
}

button {
  margin: 0 10px;
}
</style>
