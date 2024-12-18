<template>
  <TopNav />
  <main class="Layout p-6">
    <slot />
  </main>
</template>

<style lang="scss" scoped>
.Layout {
  min-height: 50vh;
}
</style>