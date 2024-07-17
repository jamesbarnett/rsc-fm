<template>
  <div class="results grid-flow" data-spacing="large">
    <h1 class="section-title">
      Your Result
    </h1>
    <p class="result-score">
      <span>76</span> of 100
    </p>
    <div class="grid-flow">
      <p class="result-rank">Great</p>
      <p>
        You scored higher than 65% of the people who have taken these tests.
      </p>
    </div>
  </div>
</template>
<style scoped>
  .section-title {
    font-weight: var(--fw-bold);
    font-size: var(--fs-600);
  }

  .result-summary {
    --padding: 2.5rem;
    --border-radius: 1.5rem;
    max-width: 46rem;
    display: grid;
  }

  @media (min-width: 600px) {
    .result-summary {
      grid-template-columns: 1fr 1fr;
      border-radius: 2rem;
      box-shadow: 0.5rem 1rem 3rem hsl(var(--clr-neutral-hsl-700), .2);
    }
  }

  .results {
    color: hsl(var(--clr-neutral-hsl-100), 0.7);
    text-align: center;
    padding: var(--padding) calc(var(--padding) * 1.5);
    background: var(--gradient-primary);
    border-radius: 0 0 var(--border-radius) var(--border-radius);
  }

  @media (min-width: 600px) {
    .results {
      border-radius: var(--border-radius);
    }
  }

  .result-score {
    display: grid;
    place-content: center;
    width: 12rem;
    margin-inline: auto;
    background: var(--gradient-to-transparent);
    aspect-ratio: 1 / 1;
    border-radius: 50%;
  }

  .result-score span {
    display: block;
    font-size: var(--fs-850);
    font-weight: var(--fw-black);
    line-height: 1;
    color: var(--clr-neutral-100);
  }

  @media (min-width: 600px) {
    .result-score span {
      font-size: var(--fs-900);
    }
  }
  .result-rank {
    color: var(--clr-neutral-100);
    font-size: var(--fs-700);
    font-weight: var(--fw-bold);
  }
</style>
