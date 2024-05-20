<script setup>
import MyHeader from './components/MyHeader.vue'
import ProductsGrid from './components/ProductsGrid.vue'
import Footer from './components/Footer.vue';
</script>
<template>
 <div>
  <header>
  <MyHeader></MyHeader>
</header>
<main class="w-full">
    <ProductsGrid></ProductsGrid>
</main>
<Footer></Footer>
 </div>
</template>
<style scoped>
</style>