<script>
import ResultSection from "./ResultSection.vue";
import DetailsSection from "./DetailsSection.vue";
export default {
  components: {
    ResultSection,
    DetailsSection,
  },
};
</script>

<template>
  <main>
    <ResultSection />
    <DetailsSection />
  </main>
</template>

<style scoped>
main {
  background-color: #fff;
  min-height: 100dvh;
}
</style>
