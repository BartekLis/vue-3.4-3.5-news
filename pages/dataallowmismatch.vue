<script setup lang="ts">
import { faker } from '@faker-js/faker';
</script>

<template>
  <!-- data-allow-mismatch doesn't work if you're using slots -->
  <Card :id="faker.string.ulid()" data-allow-mismatch>
    <template #header>
      {{ faker.lorem.words({ min: 1, max: 3 }) }}
    </template>
    {{ faker.lorem.paragraph() }}
    <p class="pt-2 text-white">
      {{ (new Date()).toDateString() }}
    </p>
  </Card>
  <CardProps :id="faker.string.ulid()"
             :header="faker.lorem.words({ min: 1, max: 3 })"
             :body="faker.lorem.paragraph()"
             data-allow-mismatch="text"
  />
  <div :id="faker.string.ulid()" data-allow-mismatch class="block max-w-sm p-6 mb-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
    <h5 class="mb-2 text-2xl font-bold capitalize tracking-tight text-gray-900 dark:text-white">
      {{ faker.lorem.words({ min: 1, max: 3 }) }}
    </h5>
    <p class="font-normal text-gray-700 dark:text-gray-400">
      {{ faker.lorem.paragraph() }}
    </p>
    <p class="pt-2 text-white">
      {{ (new Date()).toDateString() }}
    </p>
  </div>
</template>
