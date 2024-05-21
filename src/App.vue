<script setup>
import MyHeader from './components/MyHeader.vue'
import ProductsGrid from './components/ProductsGrid.vue'
import MyFooter from './components/MyFooter.vue';
</script>
<template>
 <div>
  <header>
  <MyHeader></MyHeader>
</header>
<main class="container mx-auto w-11/12">
    <ProductsGrid></ProductsGrid>
</main>
<footer>
  <MyFooter></MyFooter>
</footer>
 </div>
</template>
<style scoped>
</style>