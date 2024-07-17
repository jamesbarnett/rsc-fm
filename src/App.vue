<script setup>
import Results from './components/Results.vue'
import Summary from './components/Summary.vue'
</script>

<template>
  <main>
    <div class="result-summary">
      <Results />
      <Summary />
    </div>
  </main>
</template>

<style>
  .results-summary {
    --padding: 2.5rem;
    --border-radius: 2rem;
    max-width: 46rem;
    display: grid;
  }

  @media (min-width: 600px) {
    .result-summary {
      margin-inline: 1rem;
      grid-template-columns: 1fr 1fr;
      border-radius: var(--border-radius);
      overflow: hidden;
    box-shadow: .5rem 1rem 3rem hsl(var(--clr-neutral-hsl-700), .2);
    }
  }

</style>
