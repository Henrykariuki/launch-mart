<script setup>
import { Facebook, Instagram, Twitter } from 'lucide-vue-next';

const links = [
    {name: 'Home'},
    {name: 'About Us'},
    {name: 'Services'},
    {name: 'Contact us'},
]

const info = [
    {name: 'Nairobi, Tomboya'},
    {name: 'Street, 00100'},
    {name: 'TEL +254707070707'}
]
</script>
<template>
<div class="w-full h-auto flex justify-center px-20 bg-gray-200 flex ">
    <div class="info-container  w-full h-52 bg-gray-200 flex justify-around items-end ">
        <div class="links w-auto h-44 text-gray-800 flex flex-col items-center ">
            <p class="font-bold mt-4">Contact</p>
            <div class="flex flex-col items-center mt-4">
                <p class="hover:text-orange-600 cursor-pointer cursor-pointer" v-for="(item, index) in links" :key="index">{{ item.name }}</p>
            </div>
        </div>
        <div class="office w-auto h-44  text-gray-800 flex flex-col items-center ml-12 mr-12">
            <p class="font-bold mt-4">Nairobi Office</p>
            <div class="flex flex-col items-center mt-4">
                <p class="hover:text-orange-600 cursor-pointer" v-for="(item, index) in info" :key="index" >{{ item.name }}</p>
            </div>
        </div>
        <div class="social-icons w-auto h-44  text-gray-800 flex flex-col items-center">
            <p class="font-bold mt-4">Get in touch</p>
            <div class="flex justify-between items-center w-24 h-8 mt-10">
                <div class="w-auto h-auto hover:scale-95 duration-100 cursor-pointer"><Facebook /></div>
                <div class="w-auto h-auto hover:scale-95 duration-100 cursor-pointer"><Instagram /></div>
                <div class="w-auto h-auto hover:scale-95 duration-100 cursor-pointer"><Twitter /></div>
            </div>
        </div>
    </div>
</div>
</template>
<style scoped>
</style>