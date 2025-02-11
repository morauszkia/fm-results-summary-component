<script>
import ResultItem from "./ResultItem.vue";

export default {
  components: {
    ResultItem,
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
  <ul>
    <ResultItem
      v-for="result in results"
      :key="result.category.toLowerCase()"
      :icon="result.icon"
      :category="result.category"
      :score="result.score"
    />
  </ul>
</template>

<style scoped>
ul {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
</style>
