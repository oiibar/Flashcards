<!-- src/views/Home.vue -->
<template>
  <div>
    <h1>Flashcards App</h1>
    <FlashcardsList :cards="cards" />
  </div>
</template>

<script>
import FlashcardsList from "@/components/FlashcardsList.vue";

export default {
  components: {
    FlashcardsList,
  },
  data() {
    return {
      cards: [
        { question: "What is the capital of France?", answer: "Paris" },
        {
          question: "Who wrote Romeo and Juliet?",
          answer: "William Shakespeare",
        },
        {
          question: "Almaty or Oskemen",
          answer: "Oskemen",
        },
        // Add more flashcards as needed
      ],
    };
  },
};
</script>
