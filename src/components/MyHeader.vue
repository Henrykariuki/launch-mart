<script setup>
import { Search, ChevronDown,  MapPin, UserPlus, ShoppingCart, X, Phone } from 'lucide-vue-next'
const tags = [
    {name: 'Home'},
    {name: 'Collections'},
    {name: 'Page'},
    {name: 'Hot Offers'},
    {name: 'Blog'},
    {name: 'Contact'}
]
</script>
<template>
    <div class=" w-full h-auto px-12 py-5">
        <div class="w-full flex justify-between h-20 ">
            <div class="section-one flex justify-between items-center w-auto h-auto">
                    <div class="logo font-bold text-lg mr-4">Launch Mart</div>
                    <div class="section-one-btns flex items-center">
                        <button class="category bg-gray-100 border-solid border border-gray-500 flex justify-between px-4 py-2 rounded-l-lg text-gray-600">Category<ChevronDown /></button>
                        <input class="py-2 pl-4 pr-14 bg-gray-100 border-gray-500 border-solid border-y" type="text" placeholder="What are you looking for...">
                        <button class="search-btn px-4 py-2 bg-gray-100 border-solid border border-gray-500  rounded-r-lg"><Search class="text-gray-600" /></button>
                    </div>
            </div>
            <div class="section-two flex justify-between items-center w-auto h-auto">
                    <div class="section-two-btns flex justify-between px-4 py-2 "><MapPin class="mr-2" />Nairobi, kenya</div>
                    <div class="section-two-btns px-4 py-2">English - USD</div>
                    <div class="section-two-btns flex justify-between px-2 py-2"><UserPlus class="mr-2"/>Sign up</div>
                    <div class="section-two-btns flex justify-between px-6 py-2 bg-orange-600 rounded-lg"><ShoppingCart class="mr-1" />Cart</div>
            </div>
        </div>
        <nav class="nav-list w-full h-16  flex justify-between items-center">
            <div >
                <ul class=" w-auto h-auto flex p-2" >
                    <li class="px-2 py-1 rounded-md hover:border hover:border-solid hover:border-black hover:text-orange-600 duration-150 mr-2 text-gray-700" v-for="tag in tags">{{ tag.name }}</li>
                </ul>
            </div>
            <div class="contact border-solid border border-green-800 w-auto h-auto flex items-center text-gray-700"><Phone class="mr-1" size="16px" />+254707070707</div>
        </nav>
        <div class=" w-full h-20" >
            <p class="text-3xl font-bold mt-6">Products</p>
        </div>
        <div class="filter  flex justify-between h-12 items-center">
            <div class="right flex ml-1">
                <div class="hover:border hover:border-solid hover:border-black hover:bg-gray-100 duration-150 flex items-center mr-2 text-gray-500 px-2 rounded-md">Price<ChevronDown size="20px" class="ml-1" /></div>
                <div class="hover:border hover:border-solid hover:border-black hover:bg-gray-100 duration-150 flex items-center mr-2 text-gray-500 px-2 py-1 rounded-md">Color<ChevronDown size="20px" class="ml-1" /></div>
                <div class="hover:border hover:border-solid hover:border-black hover:bg-gray-100 duration-150 flex items-center mr-2 text-gray-500 px-2 rounded-md">Brand<ChevronDown size="20px" class="ml-1" /></div>
                <div class="hover:border hover:border-solid hover:border-black hover:bg-gray-100 duration-150 flex items-center mr-2 text-gray-500 px-2 rounded-md">warranty Type<ChevronDown size="20px" class="ml-1" /></div>
                <div class="hover:border hover:border-solid hover:border-black hover:bg-gray-100 duration-150 flex items-center mr-2 text-gray-500 px-2 rounded-md">Rating<ChevronDown size="20px" class="ml-1"/></div>
                <div class="hover:border hover:border-solid hover:border-black hover:bg-gray-100 duration-150 flex items-center mr-2 text-gray-500 px-2 rounded-md">Availability<ChevronDown size="20px" class="ml-1"/></div>
                <div class="hover:border hover:border-solid hover:border-black hover:bg-gray-100 duration-150 flex items-center mr-2 text-gray-500 px-2 rounded-md">Delivery Speed<ChevronDown size="20px" class="ml-1"/></div>
            </div>
            <div class="left">
                <div class=" flex items-center "><p class="text-gray-500">Sort by :</p><span class=" font-semibold ml-1">Relevance</span><ChevronDown size="20px" /></div>
            </div>
        </div>
        <div class=" w-full h-12 flex items-center">
                <div class=" w-auto flex items-center  h-10" >
                    <div class="border-solid border border-black hover:bg-gray-200 mr-2 rounded-xl flex items-center px-2 text-gray-500">CeraVe<X size="16px" /></div>
                    <div class="border-solid border border-black hover:bg-gray-200 mr-2 rounded-xl flex items-center px-2 text-gray-500">Red<X size="16px" /></div>
                    <div class="border-solid border border-black hover:bg-gray-200 mr-2 rounded-xl flex items-center px-2 text-gray-500">In-stock<X size="16px" /></div>
                    <div class="border-solid border border-black hover:bg-gray-200 mr-2 rounded-xl flex items-center px-2 text-gray-500">Rating: 5 & up<X size="16px" /></div>
                    <div class="border-solid border border-black hover:bg-gray-200 mr-2 rounded-xl flex items-center px-2 text-gray-500">2 Days<X size="16px" /></div>
                    <div class=" px-2"><p class="underline text-gray-500 hover:text-orange-600">Clear all</p></div>
                </div>
        </div>
    </div>
</template>
<style scoped>
.section-one, .section-two {
    
}
input {
    
}
.category, .search-btn {
   
}
.section-two-btns {
    
   
}
</style>