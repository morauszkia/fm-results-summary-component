<script>
import ResultSection from "./ResultSection.vue";
import DetailsSection from "./DetailsSection.vue";

import resultsJSON from "../data/data.json";

export default {
  data() {
    return {
      results: resultsJSON,
    };
  },
  computed: {
    average() {
      return Math.round(
        this.results.reduce((sum, next) => sum + next.score, 0) /
          this.results.length
      );
    },
  },
  components: {
    ResultSection,
    DetailsSection,
  },
};
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
</style>
