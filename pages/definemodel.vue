<script setup lang="ts">
const header = ref('')
const body = ref ('')
</script>

<template>
  <div>
    <label for="header" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Header</label>
    <input v-model="header" type="text" id="header" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Header" required />
  </div>
  <div>
    <label for="body" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Body</label>
    <input v-model="body" type="text" id="body" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Body" required />
  </div>

  <CardModel v-model="body" v-model:header="header" class="mt-6" />
</template>
