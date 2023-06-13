<script setup>
import MainHeader from './main-header.vue';
import MainFooter from './main-footer.vue'
</script>
<template>
  <main-header></main-header>

  <div
    id="main-content"
    class="relative"
  >
    <slot name="mainContent"></slot>
  </div>

<main-footer></main-footer>
</template>