<script setup>
import Attribution from "./components/Attribution.vue";
</script>

<template>
  <main>
    <section>
      <h1>Your Result</h1>
      <div><span>76</span><span>of 100</span></div>
      <p>Great</p>
      <p>
        You scored higher than 65% of the people who have taken these tests.
      </p>
    </section>
    <section>
      <h2>Summary</h2>
      <ul>
        <li>Reaction 80 / 100</li>
        <li>Memory 92 / 100</li>
        <li>Verbal 61 / 100</li>
        <li>Visual 72 / 100</li>
      </ul>
      <button>Continue</button>
    </section>
  </main>

  <Attribution />
</template>

<style scoped></style>
