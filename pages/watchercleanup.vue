<script setup lang="ts">
import { watch, onWatcherCleanup } from 'vue'

const count = ref(0)
const cleanupCount = ref(0)

watch(count, () => {
  console.log('watcher');

  onWatcherCleanup(() => {
    console.log('onWatcherCleanup');
    cleanupCount.value++
  })
})

/*
watch(id, (newId) => {
  const controller = new AbortController()

  fetch(`/api/${newId}`, { signal: controller.signal }).then(() => {
    // callback logic
  })

  onWatcherCleanup(() => {
    // abort stale request
    controller.abort()
  })
})
*/
</script>

<template>
  <button @click="count++" type="button" class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800">
    Increment
  </button>
  <p class="mt-4">
    Count: {{ count }}
  </p>
  <p class="mt-4">
    Cleanup count: {{ cleanupCount }}
  </p>
</template>
