<template>
  <div>
    <p>{{ product.title }}</p>
    <p>{{ product.price }}</p>
    <p>{{ product.id }}</p>
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const productURL = `https://fakestoreapi.com/products/${id}`;
const { data: product } = await useFetch(productURL, { key: id });
</script>

<style lang="scss" scoped></style>
