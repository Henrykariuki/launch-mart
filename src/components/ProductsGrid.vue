<script setup>
import ProductCard from "./ProductCard.vue"

const products = [
    {
        image: '/images/image-01.jpg',
        price: 2500,
        about: 'New Balance Men\'s 520 V8 Running Shoe',
        previousPrice: 2500,
        discount: 10
    },
    {
        image: '/images/image-02.jpg',
        price: 200,
        about: 'New Balance Men\'s 520 V8 Running Shoe',
        previousPrice: 400,
        discount: 12
    },
    {
        image: 'images/image-03.jpg',
        price: 3000,
        about: 'New Balance Men\'s 520 V8 Running Shoe',
        previousPrice:2500,
        discount: 5
    },
    {
        image: 'images/image-04.jpg',
        price: 3000,
        about: 'New Balance Men\'s 520 V8 Running Shoe',
        previousPrice:2500,
        discount: 25
    },
    {
        image: 'images/image-05.jpg',
        price: 3000,
        about: 'New Balance Men\'s 520 V8 Running Shoe',
        previousPrice:2500,
        discount: 15
    },
    {
        image: 'images/image-06.jpg',
        price: 3000,
        about: 'New Balance Men\'s 520 V8 Running Shoe',
        previousPrice:2500,
        discount: 40
    },
    {
        image: 'images/image-07.jpg',
        price: 3000,
        about: 'New Balance Men\'s 520 V8 Running Shoe',
        previousPrice:2500,
        discount: 6
    },
    {
        image: 'images/image-08.jpg',
        price: 3000,
        about: 'New Balance Men\'s 520 V8 Running Shoe',
        previousPrice:2500,
        discount: 10
    },
    {
        image: 'images/image-09.jpg',
        price: 3000,
        about: 'New Balance Men\'s 520 V8 Running Shoe',
        previousPrice:2500,
        discount: 4
    },
    {
        image: 'images/image-10.jpg',
        price: 3000,
        about: 'New Balance Men\'s 520 V8 Running Shoe',
        previousPrice:2500,
        discount: 8
    }
]

</script>
<template>
<div class="border border-cyan-800 w-full h-auto mt-4 grid grid-cols-5 gap-6 px-12 ">
    <ProductCard v-for="(item, index) in products" :key="index"
    :product="item"/>
</div>
</template>
<style scoped>
</style>