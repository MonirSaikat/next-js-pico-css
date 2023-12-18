<template>
  <NuxtLoadingIndicator />
  <Header />

  <main class="container">
    <NuxtPage />
  </main>
</template>

<script setup>
import("~/assets/css/pico.min.css");

useHead({
  htmlAttrs: {
    "data-theme": "light",
  },
});
</script>
