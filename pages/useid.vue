<script setup lang="ts">
import { useId } from 'vue'

const id = Math.random()
// const id = useId()
const id2 = useId()
const id3 = useId()

const ariaDescription = 'This feature has been frequently requested in the past'
</script>

<template>
  <h1 class="mb-8 text-2xl font-bold">
    Id example!
  </h1>

  <!-- v-bind Same-name Shorthand -->
  <p :id :aria-description class="text-xl p-4">
    Magni sustineo utique quis cernuus tum.
  </p>

  <p :id="id2" class="text-xl p-4">
    Similique stella tabesco conservo vaco dolor vereor tametsi viridis.
  </p>

  <p :id="id3" class="text-xl p-4">
    Tantum ago earum defero comptus.
  </p>
</template>
