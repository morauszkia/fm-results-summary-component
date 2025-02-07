<script>
export default {
  props: {
    category: String,
    score: Number,
    icon: String,
  },
  methods: {
    getImageUrl(path) {
      return new URL(path, import.meta.url).href;
    },
  },
};
</script>

<template>
  <li>
    <span>
      <img :src="getImageUrl(icon)" :alt="`${category} icon`" />
      {{ category }}
    </span>
    <span> {{ score }} / 100 </span>
  </li>
</template>
