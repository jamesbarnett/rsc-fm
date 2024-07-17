<script setup>
import { ref } from 'vue'
import SummaryItem from "./SummaryItem.vue"
import Button from "./Button.vue"
</script>
<template>
  <div class="summary grid-flow" data-spacing="large">
    <h2 class="section-title">Summary</h2>
    <div class="grid-flow">
      <SummaryItem num="1" accent="accent-1" title="Reaction" score="80" />
      <SummaryItem num="2" accent="accent-2" title="Memory" score="92" />
      <SummaryItem num="3" accent="accent-3" title="Verbal" score="61" />
      <SummaryItem num="4" accent="accent-4" title="Visual" score="72" />
    </div>
    <Button />
  </div>
</template>
<style scoped>
  .summary {
    padding: var(--padding);
  }
</style>
