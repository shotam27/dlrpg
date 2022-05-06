<script setup lang="ts">
import { ref } from "vue";

const count = ref(0);
const cards = ["cada", "cadb"];

const increment = () => {
  count.value++;
};

const decrement = () => {
  console.log("in");
  count.value--;
};
</script>

<template>
  <div class="game">
    <div class="p-2 bg-gray-100 flex justify-around">
      <div class="p-2 card" v-for="card in cards">{{ card }}</div>
    </div>
  </div>
</template>

<style>
div {
  border-radius: 10px;
}
.game {
  width: 100%;
}
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  border: solid black;
  background: gray;
  color: white;
  height: 140px;
  width: 100px;
  transform: scale(0.7);
}
</style>
