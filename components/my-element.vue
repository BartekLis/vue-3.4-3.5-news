<script setup lang="ts">
import { defineCustomElement } from 'vue'

const MyElement = defineCustomElement({
  template: `<div>hello</div>`,
  styles: [`background-color: green; width: 150px; height: 150px;`],
  // the following options are 3.5+
  shadowRoot: false, // defaults to true. Set to false to render the custom element without a shadow root. This means <style> in custom element SFCs will no longer be encapsulated.
  nonce: 'nonce-attr', // if provided, will be set as the nonce attribute on style tags injected to the shadow root.
  configureApp(app) { // a function that can be used to configure the Vue app instance for the custom element.
    app.config.errorHandler = () => console.log('my-element error')
  }
})

customElements.define('my-element', MyElement)
</script>

<template>
  <my-element />
</template>