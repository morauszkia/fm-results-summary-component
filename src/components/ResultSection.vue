<script>
export default {
  props: {
    average: {
      type: Number,
      required: true,
    },
  },
};
</script>

<template>
  <section>
    <h1>Your Result</h1>
    <div>
      <span>{{ average }}</span> <span>of 100</span>
    </div>
    <p>Great</p>
    <p>You scored higher than 65% of the people who have taken these tests.</p>
  </section>
</template>

<style></style>
