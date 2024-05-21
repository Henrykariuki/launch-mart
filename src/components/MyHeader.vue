<script setup>
import { Search, ChevronDown,  MapPin, UserPlus, ShoppingCart, X, Phone, Menu } from 'lucide-vue-next'
import { ref } from 'vue';
const tags = [
    {name: 'Home', hasSubMenu: false},
    {name: 'Collections', hasSubMenu: true},
    {name: 'Page', hasSubMenu: true},
    {name: 'Hot Offers', hasSubMenu: false},
    {name: 'Blog', hasSubMenu: true},
    {name: 'Contact', hasSubMenu: false}
]

const filters = [
    {number: 1, name: 'Price'},
    {number: 2, name: 'Color'},
    {number: 3, name: 'Brand'},
    {number: 4, name: 'Warranty Type'},
    {number: 5, name: 'Rating'},
    {number: 6, name: 'Availability'},
    {number: 7, name: 'Delivery Speed'}
]

const filterbuttons = [
    {number: 1, name: 'CeraVe', hasButton: false},
    {number: 2, name: 'Red', hasButton: true},
    {number: 3, name: 'In-stock', hasButton: false},
    {number: 4, name: 'Rating: 5 & up', hasButton: false},
    {number: 5, name: '2 Days', hasButton: false}
]

const open = ref(false)

const menuOpen = ()=> {
    open.value = !open.value
}
</script>
<template>
     <div class="full-divider border-b border-slate-300 lg:px-12">
        <div class="w-full flex justify-between h-20">
            <div class="section-one flex justify-between items-center w-auto h-auto">
                    <div class="logo font-bold text-lg mr-4">Launch Mart</div>
                    <div class="section-one-btns hidden md:flex lg:flex flex items-center">
                        <button class="category bg-gray-100 hover:bg-gray-200 border-solid border border-gray-500 flex justify-between px-4 py-2 rounded-l-lg text-gray-600">Category<ChevronDown /></button>
                        <input class="cursor-text hover:border-black py-2 pl-4 pr-14 bg-gray-100 border-gray-500 border-solid border-y" type="text" placeholder="What are you looking for...">
                        <button class="search-btn px-4 py-2 bg-gray-100 hover:bg-gray-200 border-solid border border-gray-500  rounded-r-lg"><Search class="text-gray-600" /></button>
                    </div>
            </div>
            <div class="section-two flex justify-between items-center w-auto h-auto">
                    <div class=" hidden md:flex lg:flex  flex justify-between px-4 py-2 hover:border border-black rounded-lg hover:text-orange-600 mr-1 cursor-pointer"><MapPin class="mr-2" />Nairobi, kenya</div>
                    <div class=" hidden md:flex  lg:flex  section-two-btns px-4 py-2 hover:border border-black rounded-lg hover:text-orange-600 mr-1 cursor-pointer">English - USD</div>
                    <div class="hidden md:flex  lg:flex text-nowrap flex justify-between px-2 py-2 rounded-lg mr-2 hover:border hover:text-orange-600 mr-1 border-black cursor-pointer"><UserPlus class="mr-2"/>Sign up</div>
                    <div class="  flex justify-between px-6 py-2 bg-orange-600 rounded-lg text-white cursor-pointer"><ShoppingCart class="mr-1" />Cart</div>
            </div>
        </div>
     </div>
        <div class="full-divider full-divider border-b border-slate-300 lg:px-12">
            <nav class="nav-list w-full h-12  flex justify-between items-center">
                <div class="relative">
                    <ul class="hidden md:flex lg:flex flex" >
                        <li class="px-2 py-1 rounded-md hover:border hover:border-solid hover:border-black hover:text-orange-600 duration-150 mr-2 text-gray-700" v-for="tag in tags">
                            <div class="flex items-center cursor-pointer">{{ tag.name }} <ChevronDown size="20px" v-if="tag.hasSubMenu"/></div>
                        </li>
                    </ul>
                    <div @click="menuOpen" class="menu md:hidden"><Menu size="40px"/></div>
                    <div :class="[open ? 'left-0' : '-left-60']" class="duration-500 flex flex-col items-start rounded w-60 h-auto bg-white z-50 absolute lg:hidden left-0 top-16">
                        <div v-for="(button, index) in tags" :key="index" class="px-2 py-1 w-28 my-2 w-full flex justify-start rounded-md hover:bg-gray-200 hover:text-orange-600 items-center">{{ button.name }}</div>
                        
                    </div>
                </div>
                <div class=" hidden lg:flex contact flex items-center text-gray-700"><Phone class="mr-1" size="16px" />+254707070707</div>
                <input class="rounded lg:hidden md:hidden w-52 hover:outline mx-1 cursor-pointer py-2 pl-4 pr-14 bg-gray-100 border-gray-500 border-solid border" type="text" placeholder="What are you looking for...">
                <div class=" lg:hidden text-nowrap flex justify-between px-1 py-2 rounded-lg mr-2 hover:border hover:text-orange-600 mr-1 border-black cursor-pointer"><UserPlus class="mr-2"/>Sign up</div>
            </nav>
        </div>
        <div class="w-full h-20 lg:px-12" >
            <p class="text-3xl font-bold mt-6">Products</p>
        </div>
        <div class="filter lg:px-12 flex justify-between h-12 items-center">
            <div class="wrapper flex ml-1 w-full overflow-auto">
                <div v-for="(filter, index) in filters" :key="filter.number" class="text-nowrap cursor-pointer hover:border hover:border-solid hover:border-black hover:bg-gray-100 duration-150 flex items-center mr-2 text-gray-500 px-2 rounded-md">
                    {{ filter.name }}<ChevronDown size="20px" class="ml-1" />
                </div>
            </div>
            <div class="left hidden lg:block">
                <div class=" flex items-center "><p class="text-gray-500 text-nowrap">Sort by :</p><span class=" hover:text-orange-600 font-semibold ml-1">Relevance</span><ChevronDown size="20px" /></div>
            </div>
        </div>
        <div class=" w-full h-12 flex items-center">
                <div class="wrapper-two w-auto flex items-center lg:px-12 h-auto overflow-auto">
                    <div v-for="(button, index) in filterbuttons" :key="filterbuttons.number" class="cursor-pointer border border-black hover:bg-gray-200 mr-2 rounded-xl flex items-center px-2 text-gray-500 relative">
                        <div v-if="button.hasButton" class=" red absolute bg-red-600 p-1.5 rounded-lg left-3"></div>
                        <p class="ml-5 text-nowrap">{{ button.name }}</p><X size="16px" />
                </div>
                    <div class="cursor-pointer px-2"><p class=" text-nowrap underline text-gray-500 hover:text-orange-600">Clear all</p></div>
                </div>
        </div>
</template>
<style scoped>
.wrapper::-webkit-scrollbar {
    width: 0;
}
.wrapper-two::-webkit-scrollbar {
    width: 0;
}

</style>