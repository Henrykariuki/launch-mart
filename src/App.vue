<script setup>
import MyHeader from './components/MyHeader.vue'
import ProductsGrid from './components/ProductsGrid.vue'
import MyFooter from './components/MyFooter.vue';
</script>
<template>
 <div class="container mx-auto flex flex-col gap-8 h-screen ">
  <header>
  <MyHeader class="mx-auto w-11/12 w-2xl"></MyHeader>
</header>
<main class="mx-auto w-11/12 flex-grow">
    <ProductsGrid></ProductsGrid>
</main>
<footer>
  <MyFooter></MyFooter>
</footer>
 </div>
</template>
<style scoped>
</style>