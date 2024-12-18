<script setup lang="ts">
const links = [
  {
    to: '/',
    label: 'Home'
  },
  {
    to: '/computedstability',
    label: 'Computed stability'
  },
  {
    to: '/definemodel',
    label: 'Define model'
  },
  {
    to: '/lazyhydration',
    label: 'Lazy hydration'
  },
  {
    to: '/useid',
    label: 'Use Id'
  },
  {
    to: '/dataallowmismatch',
    label: 'Data allow mismatch'
  },
  {
    to: '/templateref',
    label: 'Template ref'
  },
  {
    to: '/watchercleanup',
    label: 'Watcher cleanup'
  },
]

const activeClasses = 'text-white bg-blue-700 rounded md:bg-transparent md:text-blue-700 md:p-0 dark:text-white md:dark:text-blue-500'
const regularClasses = 'text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent'

const route = useRoute()
</script>

<template>
  <nav class="bg-white border-gray-200 dark:bg-gray-900">
    <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
      <div class="w-full md:block md:w-auto" id="navbar-default">
        <ul class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
          <li v-for="link in links" :key="link.to">
            <NuxtLink :to="link.to" class="block py-2 px-3" :class="route.path === link.to ? activeClasses : regularClasses">
              {{ link.label }}
            </NuxtLink>
          </li>

        </ul>
      </div>
    </div>
  </nav>
</template>