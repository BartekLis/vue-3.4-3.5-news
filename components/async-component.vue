<script setup lang="ts">
import { faker } from '@faker-js/faker';
</script>

<template>
  <p>
    {{ faker.lorem.paragraph() }}
  </p>
</template>
