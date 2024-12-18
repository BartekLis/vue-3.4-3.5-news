<script setup lang="ts">
import { useTemplateRef } from 'vue'

const id = useId()
const divRef = useTemplateRef(id)

watchEffect(() => {
  if (divRef.value) {
    divRef.value.style = 'background-color: green'
  } else {
    // not mounted yet, or the element was unmounted (e.g. by v-if)
  }
})
</script>

<template>
  <div :id :ref="id" class="m-4">
    hello
  </div>
</template>
