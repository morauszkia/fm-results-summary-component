<script setup>
import { ref, computed } from "vue";

import ResultSection from "./ResultSection.vue";
import DetailsSection from "./DetailsSection.vue";

import resultsJSON from "../data/data.json";

const results = ref(resultsJSON);
const average = computed(() =>
  Math.round(
    results.value.reduce((sum, next) => sum + next.score, 0) /
      results.value.length
  )
);
</script>

<template>
  <main>
    <ResultSection :average="average" />
    <DetailsSection :results="results" />
  </main>
</template>

<style scoped>
main {
  background-color: #fff;
  min-height: 100dvh;
}

@media screen and (min-width: 32rem) {
  main {
    min-height: unset;
    border-radius: 2rem;
    overflow: hidden;
    min-width: 24rem;
  }
}

@media screen and (min-width: 50rem) {
  main {
    display: flex;
    width: 46rem;
  }
}
</style>
