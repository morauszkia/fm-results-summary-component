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
