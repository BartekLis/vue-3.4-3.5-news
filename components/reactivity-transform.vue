<script setup lang="ts">
//Reactivity Transform
//Removed Experimental Feature in 3.4
let count = $ref(0)

console.log(count)

function increment() {
  count++
}
</script>

<template>
  <button @click="increment">{{ count }}</button>
</template>