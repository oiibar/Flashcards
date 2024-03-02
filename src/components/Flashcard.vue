<!-- src/components/Flashcard.vue -->
<template>
  <div class="flashcard" @click="flipCard">
    <div class="card" :class="{ flipped: isFlipped }">
      <div class="card-content front">
        <h3>{{ card.question }}</h3>
      </div>
      <div class="card-content back">
        <p>{{ card.answer }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    card: Object,
  },
  data() {
    return {
      isFlipped: false,
    };
  },
  methods: {
    flipCard() {
      this.isFlipped = !this.isFlipped;
    },
  },
};
</script>

<style scoped>
.flashcard {
  perspective: 1000px;
  display: flex;
  justify-content: center;
  text-align: center;
  align-items: center;
}

.card {
  width: 200px;
  height: 300px;
  transform-style: preserve-3d;
  transition: transform 0.5s;
}

.card-content {
  width: 100%;
  height: 100%;
  position: absolute;
  backface-visibility: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 20px;
}

.front {
  transform: rotateY(0deg);
  background-color: #db4d52;
}

.back {
  transform: rotateY(180deg);
  background-color: #49b0e4;
}

.flipped {
  transform: rotateY(180deg);
}
</style>
