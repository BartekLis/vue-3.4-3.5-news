<script setup lang="ts">
const input = ref(0)
const evenOrOdd = computed(() => input.value % 2 === 0 ? 'Even' : 'Odd')

watchEffect(() => console.log(evenOrOdd.value))
// watch(evenOrOdd, () => console.log(evenOrOdd.value))
</script>

<template>
  <div>
    <label for="count" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Count</label>
    <input v-model="input" type="text" id="count" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="0" required />
  </div>

  <p class="mt-4">
    Input is {{ evenOrOdd }}
  </p>
</template>
