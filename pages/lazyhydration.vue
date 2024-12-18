<script setup lang="ts">
import { defineAsyncComponent, hydrateOnVisible } from 'vue'

const AsyncComp = defineAsyncComponent({
  loader: () => import('../components/async-component.vue'),
  hydrate: hydrateOnVisible()
})
</script>

<template>
  <div class="m-2">
    <p class="vh">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed luctus elit nec imperdiet varius. Donec varius mi sed purus mattis facilisis. Suspendisse ex diam, semper id tincidunt nec, tincidunt in tellus. Nullam in elit et eros egestas vestibulum et id lorem. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent eleifend dictum sagittis. Praesent nec urna dolor. Mauris consequat nibh quis tincidunt pretium.
      <br><br>
      Etiam volutpat lectus ullamcorper, gravida mauris non, rutrum magna. Sed at purus tempus, pulvinar purus in, aliquam ipsum. Integer rutrum maximus augue, eu gravida velit dignissim accumsan. Nulla elementum efficitur mauris, et imperdiet magna porta cursus. Sed nec nunc et libero aliquam pharetra. Sed pellentesque ligula sit amet blandit scelerisque. Nunc ut iaculis magna, id pretium est. Aenean neque mi, varius eget sodales vitae, lacinia eget ante. Morbi hendrerit laoreet metus, et imperdiet sapien laoreet at. Suspendisse tincidunt porta erat quis mollis. Proin volutpat tellus at odio feugiat viverra. Mauris euismod dapibus justo, et accumsan velit. Sed vehicula risus vitae nisl lobortis efficitur. Suspendisse ornare aliquet nibh et blandit.
    </p>

    <AsyncComp />
  </div>
</template>

<style scoped>
.vh {
  height: 125vh;
}
</style>