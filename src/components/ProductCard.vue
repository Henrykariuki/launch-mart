<script setup>
import { Star, StarHalf } from 'lucide-vue-next';

const props = defineProps({
    product: {
        type: Object,
        required: true
    }
})
</script>
<template>
    <div class="product-container h-auto hover:shadow-xl hover:scale-95 duration-100 px-1 cursor-pointer">
        <div class="image-container object-cover  relative ">
            <div class="bg-orange-600 text-white absolute left-2 top-1 rounded-sm px-1 text-xs">{{ product.discount }}%</div>
            <img class="rounded-xl h-60" :src="product.image">
        </div>
        <div class="product-info mt-6">
            <div class="ratings flex mb-2"><Star size="16px" /><Star size="16px" /><Star size="16px" /><Star size="16px" /><StarHalf size="16px" /><spsn class="text-gray-400 text-xs">(321)</spsn></div>
            <div class="about leading-5 text-sm mb-2">{{ product.about }}</div>
            <div class="flex justify-between items-center h-10">
                <p class="price text-nowrap text-sm font-bold">KSh{{ product.price }}<span class="line-through text-xs ml-2 text-gray-400">KSh{{ product.previousPrice }}</span></p>
                <div class="add-cart border-solid border border-gray-500 px-2 py-1 text-nowrap rounded-md text-xs">Add to cart</div>
            </div>
        </div>
    </div>
</template>
<style scoped>
</style>