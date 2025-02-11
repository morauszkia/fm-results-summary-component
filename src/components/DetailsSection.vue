<script>
import ResultsList from "./ResultsList.vue";

export default {
  components: {
    ResultsList,
  },
  props: {
    results: {
      type: Array,
      required: true,
    },
  },
};
</script>

<template>
  <section>
    <h2>Summary</h2>
    <ResultsList :results="results" />
    <button>Continue</button>
  </section>
</template>

<style scoped>
section {
  padding: 1.875rem;
  padding-top: 1.5rem;
  background-color: #fff;

  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

h2 {
  font-size: 1.125rem;
  color: #303b59;
}
</style>
