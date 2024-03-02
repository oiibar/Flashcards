<!-- src/components/FlashcardsList.vue -->
<template>
  <div>
    <Flashcard :card="currentCard" />
    <div class="button-container">
      <button @click="prevCard" :disabled="currentIndex === 0">Previous</button>
      <button @click="nextCard" :disabled="currentIndex === cards.length - 1">
        Next
      </button>
    </div>
  </div>
</template>

<script>
import Flashcard from "@/components/Flashcard.vue";

export default {
  components: {
    Flashcard,
  },
  props: {
    cards: Array,
  },
  data() {
    return {
      currentIndex: 0,
    };
  },
  computed: {
    currentCard() {
      return this.cards[this.currentIndex];
    },
  },
  methods: {
    nextCard() {
      if (this.currentIndex < this.cards.length - 1) {
        this.currentIndex++;
      }
    },
    prevCard() {
      if (this.currentIndex > 0) {
        this.currentIndex--;
      }
    },
  },
};
</script>

<style>
.button-container {
  display: flex;
  justify-content: space-between;
  margin-top: 20px;
}
</style>
