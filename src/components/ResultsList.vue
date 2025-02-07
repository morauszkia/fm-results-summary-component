<script>
import ResultItem from "./ResultItem.vue";

export default {
  components: {
    ResultItem,
  },
};
</script>

<template>
  <ul>
    <ResultItem category="Reaction" score="80" />
    <ResultItem category="Memory" score="92" />
    <ResultItem category="Verbal" score="61" />
    <ResultItem category="Visual" score="72" />
  </ul>
</template>
