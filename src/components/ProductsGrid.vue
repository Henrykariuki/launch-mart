<script setup>
import ProductCard from "./ProductCard.vue"
import {ref} from 'vue'
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
        about: 'Classic Vanilla',
        previousPrice: 400,
        discount: 12
    },
    {
        image: 'images/image-03.jpg',
        price: 3000,
        about: 'Wooden Multimedia Small Speaker 2.0usb Desktop',
        previousPrice:2500,
        discount: 5
    },
    {
        image: 'images/image-04.jpg',
        price: 3000,
        about: 'Arctic hunter RFID USB Men\'s backpack Business Travel',
        previousPrice:2500,
        discount: 25
    },
    {
        image: 'images/image-05.jpg',
        price: 3000,
        about: 'Wholesale Men\'s Varsity Jacket Button Front Letter',
        previousPrice:2500,
        discount: 15
    },
    {
        image: 'images/image-06.jpg',
        price: 3000,
        about: 'Sport Snapback Cap Casquette Hommes Baseba',
        previousPrice:2500,
        discount: 40
    },
    {
        image: 'images/image-07.jpg',
        price: 3000,
        about: 'Lettuce Hot Sales Natural Dried Lettuce Cuts Dehydrated AD Lettuce For Food',
        previousPrice:2500,
        discount: 6
    },
    {
        image: 'images/image-08.jpg',
        price: 3000,
        about: 'iMICE HD460 Gaming headset with mic Gamer',
        previousPrice:2500,
        discount: 10
    },
    {
        image: 'images/image-09.jpg',
        price: 3000,
        about: '100% cotton fabric European top foam',
        previousPrice:2500,
        discount: 4
    },
    {
        image: 'images/image-10.jpg',
        price: 3000,
        about: '2023 High Quality Custom Outdoor Streetwear Baggy',
        previousPrice:2500,
        discount: 8
    }
]

</script>
<template>
<div class="grid grid-cols-1 gap-4 sm:grid-cols-2  lg:grid-cols-5">
    <ProductCard v-for="(item, index) in products" :key="index"
    :product="item"/>
</div>
</template>
<style scoped>
</style>