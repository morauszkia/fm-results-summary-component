<script setup>
import ResultItem from "./ResultItem.vue";

const { results } = defineProps(["results"]);
</script>

<template>
  <ul>
    <ResultItem
      v-for="result in results"
      :key="result.category.toLowerCase()"
      :result="result"
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
