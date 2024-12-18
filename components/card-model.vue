<script setup lang="ts">
// const model = defineModel()
const model = defineModel({ type: String })
const header = defineModel(
    'header',
    { type: String, default: 'Header' }
)

// emits "update:modelValue" when mutated
model.value = 'hello'
</script>

<template>
  <div class="block max-w-sm p-6 mb-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
    <h5 data-allow-mismatch class="mb-2 text-2xl font-bold capitalize tracking-tight text-gray-900 dark:text-white">
      {{ header }}
    </h5>
    <p data-allow-mismatch class="font-normal text-gray-700 dark:text-gray-400">
      {{ model }}
    </p>
  </div>
</template>
