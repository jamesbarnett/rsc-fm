<script setup>
  const props = defineProps([
    "num",
    "accent",
    "title",
    "score"
  ])
</script>
<template>
  <div class="summary-item" :data-item-type="accent">
    <div class="flex-group">
      <svg class="summary-icon" xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="none" viewBox="0 0 20 20"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.25" d="M10.833 8.333V2.5l-6.666 9.167h5V17.5l6.666-9.167h-5Z"/></svg>
      <h3 class="summary-item-title">{{props.title}}</h3>
    </div>
    <p class="summary-score"><span>{{props.score}}</span> / 100</p>
  </div>
</template>
<style scoped>
  .flex-group {
    display: flex;
    align-items: center;
    gap: .5rem;
    flext-wrap: wrap;
  }
  .grid-flow {
    display: grid;
    align-content: start;
    gap: 1rem;
  }

  .grid-flow[data-spacing="large"] {
    gap: 2rem;
  }

  .summary-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    border-radius: 0.5rem;
    background-color: hsl(var(--item-color), 0.1);
  }

  .summary-item svg {
    stroke: hsl(var(--item-color));
  }

  .summary-item-title {
    color: hsl(var(--item-color));
    font-weight: var(--fw-bold);
  }

  .summary-item[data-item-type="accent-1"] {
    --item-color: var(--clr-accent-1);
  }

  .summary-item[data-item-type="accent-2"] {
    --item-color: var(--clr-accent-2);
  }

  .summary-item[data-item-type="accent-3"] {
    --item-color: var(--clr-accent-3);
  }

  .summary-item[data-item-type="accent-4"] {
    --item-color: var(--clr-accent-4);
  }

  .summary-score {
    font-weight: var(--fw-black);
    color: hsl(var(--clr-neutral-hsl-700), 0.5);
  }

  .summary-score span {
    color: var(--clr-neutral-700);
  }
</style>
