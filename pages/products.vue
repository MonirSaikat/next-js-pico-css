<template>
  <h1 v-if="pending">Loading Data</h1>
  <div v-for="product in products">
    <h2>{{ product.title }}</h2>
  </div>
</template>

<script setup>
const url = "https://dummyjson.com/products";
const { data, pending } = await useFetch(url, {
  transform: function (_data) {
    return _data.products;
  },
});

const products = data.value;
</script>
