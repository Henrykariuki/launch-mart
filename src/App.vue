<script setup>
import MyHeader from './components/MyHeader.vue'
import ProductsGrid from './components/ProductsGrid.vue'
</script>
<template>
<header>
  <MyHeader></MyHeader>
</header>
<main>
  <div class="w-full">
    <ProductsGrid></ProductsGrid>
  </div>
</main>
</template>
<style scoped>
</style>