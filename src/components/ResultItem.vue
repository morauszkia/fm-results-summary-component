<script>
export default {
  props: {
    category: String,
    score: Number,
  },
};
</script>

<template>
  <li>{{ category }} {{ score }} / 100</li>
</template>
