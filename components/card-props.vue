<script setup lang="ts">
//Before
/*const props = withDefaults(
    defineProps<{
      header?: string
      body?: string
    }>(),
    {
      header: 'Header',
      body: 'Lorem Ipsum'
    }
)*/

const { header = 'Header', body = 'Lorem Ipsum' } = defineProps<{
  header?: string
  body?: string
}>()

/*watch(header, () => {
  console.log(header)
})*/
//    ^ results in compile-time error

watch(() => header, () => {
  console.log(header)
})
//    ^ wrap in a getter, works as expected
</script>

<template>
  <div class="block max-w-sm p-6 mb-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
    <h5 data-allow-mismatch class="mb-2 text-2xl font-bold capitalize tracking-tight text-gray-900 dark:text-white">
      {{ header }}
    </h5>
    <p data-allow-mismatch class="font-normal text-gray-700 dark:text-gray-400">
      {{ body }}
    </p>
  </div>
</template>
