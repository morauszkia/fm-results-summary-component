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

button {
  --start: #303b59;
  --end: #303b59;
  background: linear-gradient(var(--start), var(--end));
  color: #fff;
  font-size: 1.125rem;
  font-weight: 700;
  padding: 1rem 0;
  border-radius: 100px;
  cursor: pointer;
  border: none;
  transition: all 0.3s;
}

button:hover,
button:focus {
  --start: #6943ff;
  --end: #2f2ce9;
  outline: 0;
}

button:active {
  transform: scale(0.95);
}
</style>
