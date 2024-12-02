<template>
    <div>
        <div class="fixed  inset-0 bg-black/50 sm:hidden z-[999999999] xl:z-[1]" 
             v-show="isSidebarOpen" 
             @click="toggleSidebar"></div>

        <aside :class="{
            '-translate-x-full': !isSidebarOpen && window.innerWidth < 1200,
            'translate-x-0': isSidebarOpen || window.innerWidth >= 1200
           }"
           class="w-72 fixed pt-20 overflow-auto pb-10 h-screen top-0 z-[2] 
                  bg-gradient-to-br from-white/20 to-black/15 backdrop-filter backdrop-blur-xl 
                  border-r border-white/20
                  shadow-[0_4px_30px_rgba(0,0,0,0.15)]
                  transition-transform duration-300 transform">
            <nav class="space-y-2 flex flex-col px-3 pt-6">
                <div class="group transition-all duration-200 ease-in-out">
                    <div class="flex px-4 py-2.5 bg-transparent hover:text-purple-800 cursor-pointer rounded-lg 
                        hover:bg-white/20 hover:backdrop-blur-3xl gap-2 items-center
                        transition-all duration-200 ease-in-out">
                        <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-width="2" d="M4 5a1 1 0 0 1 1-1h4a1 1 0 0 1 1 1v5a1 1 0 0 1-1 1H5a1 1 0 0 1-1-1zm10 0a1 1 0 0 1 1-1h4a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-4a1 1 0 0 1-1-1zM4 16a1 1 0 0 1 1-1h4a1 1 0 0 1 1 1v3a1 1 0 0 1-1 1H5a1 1 0 0 1-1-1zm10-3a1 1 0 0 1 1-1h4a1 1 0 0 1 1 1v6a1 1 0 0 1-1 1h-4a1 1 0 0 1-1-1z"/></svg>
                        <a href="#" class="block text-sm font-semibold">Dashboard</a>
                    </div>
                </div>
                <div class="group transition-all duration-200 ease-in-out">
                    <div class="flex px-4 justify-between py-2 hover:text-purple-800 cursor-pointer group rounded-lg hover:bg-white/30 hover:backdrop-blur-3xl gap-2 items-center" @click="toggleDropdown('profiles')">
                        <div class="flex items-center gap-2 justify-between">
                            <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-dasharray="28" stroke-dashoffset="28" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><path d="M4 21v-1c0 -3.31 2.69 -6 6 -6h4c3.31 0 6 2.69 6 6v1"><animate fill="freeze" attributeName="stroke-dashoffset" dur="0.4s" values="28;0"/></path><path d="M12 11c-2.21 0 -4 -1.79 -4 -4c0 -2.21 1.79 -4 4 -4c2.21 0 4 1.79 4 4c0 2.21 -1.79 4 -4 4Z"><animate fill="freeze" attributeName="stroke-dashoffset" begin="0.4s" dur="0.4s" values="28;0"/></path></g></svg>
                            <a href="#" class="block text-sm font-semibold  ">Profiles & Groups</a>
                        </div>
                        <svg class="size-4 transition-transform" :class="{ 'rotate-180': dropdowns.profiles }" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M18 9s-4.419 6-6 6s-6-6-6-6" color="currentColor"/></svg>
                    </div>
                    <div v-if="dropdowns.profiles" class="pl-8">
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Profile 1
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Profile 2
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Profile 3
                        </a>
                    </div>
                </div>
                <div class="group transition-all duration-200 ease-in-out">
                    <div class="flex px-4 justify-between py-2 hover:text-purple-800 cursor-pointer group rounded-lg hover:bg-white/30 hover:backdrop-blur-3xl gap-2 items-center" @click="toggleDropdown('categories')">
                        <div class="flex items-center gap-2 justify-between">
                            <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
                                <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M7 7h9.75c2.107 0 3.16 0 3.917.506a3 3 0 0 1 .827.827C22 9.09 22 10.143 22 12.25c0 3.511 0 5.267-.843 6.528a5 5 0 0 1-1.38 1.38C18.518 21 16.762 21 13.25 21H12c-4.714 0-7.071 0-8.536-1.465C2 18.072 2 15.715 2 11V7.944c0-1.816 0-2.724.38-3.406A3 3 0 0 1 3.538 3.38C4.22 3 5.128 3 6.944 3C8.108 3 8.69 3 9.2 3.191c1.163.436 1.643 1.493 2.168 2.542L12 7" color="currentColor"/>
                            </svg>
                            <a href="#" class="block text-sm font-semibold">Categories</a>
                        </div>
                        <svg class="size-4 transition-transform" :class="{ 'rotate-180': dropdowns.categories }" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
                            <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M18 9s-4.419 6-6 6s-6-6-6-6"/>
                        </svg>
                    </div>
                    <div v-if="dropdowns.categories" class="pl-8">
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Category 1
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Category 2
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Category 3
                        </a>
                    </div>
                </div>
                <div class="group transition-all duration-200 ease-in-out">
                    <div class="flex px-4 justify-between py-2 hover:text-purple-800 cursor-pointer group rounded-lg hover:bg-white/30 hover:backdrop-blur-3xl gap-2 items-center" @click="toggleDropdown('brands')">
                        <div class="flex items-center gap-2 justify-between">
                            <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 48 48"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"><path d="M4 13L24 8L44 13L24 18L4 13Z"/><path d="M13 16V25.9706C13 25.9706 18 29 24 29C30 29 35 25.9706 35 25.9706V16"/><path d="M7 14V36"/><rect width="6" height="6" x="4" y="34" fill="currentColor"/></g></svg>
                            <a href="#" class="block text-sm font-semibold  ">Brands</a>
                        </div>
                        <svg class="size-4 transition-transform" :class="{ 'rotate-180': dropdowns.brands }" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M18 9s-4.419 6-6 6s-6-6-6-6" color="currentColor"/></svg>
                    </div>
                    <div v-if="dropdowns.brands" class="pl-8">
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Brand 1
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Brand 2
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Brand 3
                        </a>
                    </div>
                </div>
                <div class="group transition-all duration-200 ease-in-out">
                    <div class="flex px-4 justify-between py-2 hover:text-purple-800 cursor-pointer group rounded-lg hover:bg-white/30 hover:backdrop-blur-3xl gap-2 items-center" @click="toggleDropdown('stores')">
                        <div class="flex items-center gap-2 justify-between">
                            <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 14 14"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M1.5 8.5V13a.5.5 0 0 0 .5.5h10a.5.5 0 0 0 .5-.5V8.5M13 6H1a.5.5 0 0 1-.5-.5v-2l1.22-2.45a1 1 0 0 1 .9-.55h8.76a1 1 0 0 1 .9.55L13.5 3.5v2a.5.5 0 0 1-.5.5M8 8.5v5M1.5 10H8M.5 3.5h13"/></svg>
                            <a href="#" class="block text-sm font-semibold  ">Stores</a>
                        </div>
                        <svg class="size-4 transition-transform" :class="{ 'rotate-180': dropdowns.stores }" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M18 9s-4.419 6-6 6s-6-6-6-6" color="currentColor"/></svg>
                    </div>
                    <div v-if="dropdowns.stores" class="pl-8">
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Store 1
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Store 2
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Store 3
                        </a>
                    </div>
                </div>
                <div class="group transition-all duration-200 ease-in-out">
                    <div class="flex px-4 justify-between py-2 hover:text-purple-800 cursor-pointer group rounded-lg hover:bg-white/30 hover:backdrop-blur-3xl gap-2 items-center" @click="toggleDropdown('attributes')">
                        <div class="flex items-center gap-2 justify-between">
                            <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 56 56"><path fill="currentColor" d="M19.41 20.406c4.266 0 7.828-3.539 7.828-7.804s-3.562-7.829-7.828-7.829c-4.289 0-7.851 3.563-7.851 7.829c0 4.265 3.562 7.804 7.851 7.804m17.18 0c4.265 0 7.828-3.539 7.828-7.804s-3.562-7.829-7.828-7.829s-7.828 3.563-7.828 7.829c0 4.265 3.562 7.804 7.828 7.804m-17.18-3.773c-2.226 0-4.078-1.852-4.078-4.031c0-2.204 1.852-4.055 4.078-4.055c2.203 0 4.055 1.851 4.055 4.055c0 2.18-1.852 4.03-4.055 4.03m17.18 0c-2.203 0-4.055-1.852-4.055-4.031c0-2.204 1.852-4.055 4.055-4.055s4.055 1.851 4.055 4.055c0 2.18-1.852 4.03-4.055 4.03m-8.602 19.195c4.266 0 7.852-3.562 7.852-7.828s-3.586-7.852-7.852-7.852c-4.265 0-7.828 3.586-7.828 7.852s3.563 7.828 7.828 7.828m-17.18 0c4.266 0 7.829-3.562 7.829-7.828s-3.563-7.852-7.828-7.852S2.98 23.734 2.98 28s3.562 7.828 7.828 7.828m34.36 0c4.289 0 7.852-3.562 7.852-7.828s-3.563-7.852-7.852-7.852c-4.266 0-7.828 3.586-7.828 7.852s3.562 7.828 7.828 7.828m-17.18-3.773c-2.226 0-4.078-1.851-4.078-4.055s1.851-4.078 4.078-4.078s4.078 1.875 4.078 4.078s-1.875 4.055-4.078 4.055m-17.18 0c-2.203 0-4.055-1.852-4.055-4.055s1.851-4.078 4.055-4.078s4.054 1.875 4.054 4.078s-1.851 4.055-4.054 4.055m34.36 0c-2.203 0-4.055-1.852-4.055-4.055s1.852-4.078 4.055-4.078c2.227 0 4.078 1.875 4.078 4.078s-1.851 4.055-4.078 4.055M19.41 51.227c4.266 0 7.828-3.563 7.828-7.852c0-4.266-3.562-7.805-7.828-7.805c-4.289 0-7.851 3.54-7.851 7.805c0 4.29 3.562 7.852 7.851 7.852m17.18 0c4.265 0 7.828-3.563 7.828-7.852c0-4.266-3.562-7.805-7.828-7.805s-7.828 3.54-7.828 7.805c0 4.29 3.562 7.852 7.828 7.852m-17.18-3.774c-2.226 0-4.078-1.851-4.078-4.078c0-2.18 1.852-4.031 4.078-4.031c2.203 0 4.055 1.851 4.055 4.031c0 2.227-1.852 4.078-4.055 4.078m17.18 0c-2.203 0-4.055-1.851-4.055-4.078c0-2.18 1.852-4.031 4.055-4.031s4.055 1.851 4.055 4.031c0 2.227-1.852 4.078-4.055 4.078"/></svg>
                            <a href="#" class="block text-sm font-semibold  ">Attibutes</a>
                        </div>
                        <svg class="size-4 transition-transform" :class="{ 'rotate-180': dropdowns.attributes }" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M18 9s-4.419 6-6 6s-6-6-6-6" color="currentColor"/></svg>
                    </div>
                    <div v-if="dropdowns.attributes" class="pl-8">
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Attribute 1
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Attribute 2
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Attribute 3
                        </a>
                    </div>
                </div>
                <div class="group transition-all duration-200 ease-in-out">
                    <div class="flex px-4 justify-between py-2 hover:text-purple-800 cursor-pointer group rounded-lg hover:bg-white/30 hover:backdrop-blur-3xl gap-2 items-center" @click="toggleDropdown('products')">
                        <div class="flex items-center gap-2 justify-between">
                            <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="M7 2H3a1 1 0 0 0-1 1v18a1 1 0 0 0 1 1h4a1 1 0 0 0 1-1V3a1 1 0 0 0-1-1M5 21a2 2 0 1 1 2-2a2 2 0 0 1-2 2m2-9H3V3h4Zm-1 7a1 1 0 1 1-1-1a1 1 0 0 1 1 1m8-17h-4a1 1 0 0 0-1 1v18a1 1 0 0 0 1 1h4a1 1 0 0 0 1-1V3a1 1 0 0 0-1-1m-2 19a2 2 0 1 1 2-2a2 2 0 0 1-2 2m2-9h-4V3h4Zm-1 7a1 1 0 1 1-1-1a1 1 0 0 1 1 1"/></svg>
                            <a href="#" class="block text-sm font-semibold  ">Products</a>
                        </div>
                        <svg class="size-4 transition-transform" :class="{ 'rotate-180': dropdowns.products }" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M18 9s-4.419 6-6 6s-6-6-6-6" color="currentColor"/></svg>
                    </div>
                    <div v-if="dropdowns.products" class="pl-8">
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Product 1
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Product 2
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Product 3
                        </a>
                    </div>
                </div>
                <div class="group transition-all duration-200 ease-in-out">
                    <div class="flex px-4 justify-between py-2 hover:text-purple-800 cursor-pointer group rounded-lg hover:bg-white/30 hover:backdrop-blur-3xl gap-2 items-center" @click="toggleDropdown('orders')">
                        <div class="flex items-center gap-2 justify-between">
                            <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="M16 12h2v4h-2z"/><path fill="currentColor" d="M20 7V5c0-1.103-.897-2-2-2H5C3.346 3 2 4.346 2 6v12c0 2.201 1.794 3 3 3h15c1.103 0 2-.897 2-2V9c0-1.103-.897-2-2-2M5 5h13v2H5a1.001 1.001 0 0 1 0-2m15 14H5.012C4.55 18.988 4 18.805 4 18V8.815c.314.113.647.185 1 .185h15z"/></svg>
                            <a href="#" class="block text-sm font-semibold  ">Orders</a>
                        </div>
                        <svg class="size-4 transition-transform" :class="{ 'rotate-180': dropdowns.orders }" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M18 9s-4.419 6-6 6s-6-6-6-6" color="currentColor"/></svg>
                    </div>
                    <div v-if="dropdowns.orders" class="pl-8">
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Order 1
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Order 2
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Order 3
                        </a>
                    </div>
                </div>
                <div class="group transition-all duration-200 ease-in-out">
                    <div class="flex px-4 justify-between py-2 hover:text-purple-800 cursor-pointer group rounded-lg hover:bg-white/30 hover:backdrop-blur-3xl gap-2 items-center" @click="toggleDropdown('carts')">
                        <div class="flex items-center gap-2 justify-between">
                            <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="M4 20V7.1L2.05 2.85L3.85 2L6.2 7.05h11.6L20.15 2l1.8.85L20 7.1V20zm6-7h4q.425 0 .713-.288T15 12t-.288-.712T14 11h-4q-.425 0-.712.288T9 12t.288.713T10 13m-4 5h12V9.05H6zm0 0V9.05z"/></svg>
                            <a href="#" class="block text-sm font-semibold  ">Carts</a>
                        </div>
                        <svg class="size-4 transition-transform" :class="{ 'rotate-180': dropdowns.carts }" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M18 9s-4.419 6-6 6s-6-6-6-6" color="currentColor"/></svg>
                    </div>
                    <div v-if="dropdowns.carts" class="pl-8">
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Cart 1
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Cart 2
                        </a>
                        <a href="#" class="block bg-transparent py-2 flex items-center gap-2
                            hover:bg-white/20 active:bg-white/25
                            rounded-lg hover:backdrop-blur-md pl-2.5 text-gray-700 text-sm
                            transition-all duration-200">
                            <div class="size-1.5 bg-blue-800 rounded-full shrink-0"></div>Cart 3
                        </a>
                    </div>
                </div>
            </nav>
        
            <div class="px-2 mt-10 sm:mx-4">
                <div class="px-2 py-10 text-center rounded-3xl 
                    bg-gray-100/80  backdrop-blur-[1px] 
                    shadow-sm border border-white/20
                    hover:bg-white/15 transition-all duration-300">
                    <button class="w-full py-2 font-medium">Add files</button>
                    <p class="text-[12px]">Pallentesque Habitant<br>Morbi Trisque Senectus Et</p>
                    <div class="size-10 cursor-pointer mt-3 mx-auto flex items-center justify-center rounded-full bg-white/80">
                        <svg class="size-5" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
                            <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 5v14m-7-7h14"/>
                        </svg>
                    </div>
                </div>
            </div>
        </aside>
    </div>
</template>

<script>
export default {
  props: {
    modelValue: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      isSidebarOpen: this.modelValue,
      activeItem: null,
      dropdowns: {
        categories: false,
        profiles: false,
        brands: false,
        stores: false,
        attributes: false,
        products: false,
        orders: false,
        carts: false
      },
      window: window
    };
  },
  watch: {
    modelValue(newVal) {
      this.isSidebarOpen = newVal;
    }
  },
  methods: {
    toggleSidebar() {
      this.isSidebarOpen = !this.isSidebarOpen;
      this.$emit('update:modelValue', this.isSidebarOpen);
    },
    toggleDropdown(name) {
      this.dropdowns[name] = !this.dropdowns[name];
      this.activeItem = name;
    },
  },
  mounted() {
    this.$router?.beforeEach(() => {
      this.isSidebarOpen = false;
      this.$emit('update:modelValue', false);
    });
  },
};
</script>
<style scoped>
.size-5 {
    width: 1.5em;
    height: 1.5em;
}

.size-4 {
    width: 1.125rem;
    height: 1.125rem;
}

/* Add custom text size */
.text-sm {
    font-size: 0.9375rem !important; /* Changed from 0.875rem (14px) to 0.9375rem (15px) */
    line-height: 1.25rem;
}

::-webkit-scrollbar{
  display: none;
}

/* Add smooth transitions */
.nav-item {
    @apply transition-all duration-200 ease-in-out;
}

/* Enhanced shiny glass effect */
.glass-effect {
    @apply bg-gradient-to-br from-white/20 to-black/15
           backdrop-filter backdrop-blur-xl 
           border border-white/20
           shadow-[0_4px_30px_rgba(0,0,0,0.15)]
           after:absolute after:inset-0 
           after:bg-gradient-to-t after:from-transparent after:to-white/5
           after:pointer-events-none;
}

/* Add hover animations */
.hover-scale {
    @apply hover:scale-105 transition-transform duration-200;
}

/* Improved scrollbar styling */
::-webkit-scrollbar {
    width: 5px;
}

::-webkit-scrollbar-track {
    @apply bg-transparent;
}

::-webkit-scrollbar-thumb {
    @apply bg-gradient-to-b from-white/50 to-white/30 rounded-full;
}

/* Add support for Firefox */
* {
    scrollbar-width: thin;
    scrollbar-color: rgba(255, 255, 255, 0.4) transparent;
}

/* Optional: Add subtle text shadow for better readability */
.text-sm {
    text-shadow: 0 1px 1px rgba(0, 0, 0, 0.1);
}

/* Shiny hover effect */
.hover-glass {
    @apply hover:bg-gradient-to-br hover:from-white/25 hover:to-black/20
           hover:backdrop-blur-lg 
           hover:shadow-[0_8px_32px_rgba(0,0,0,0.2)]
           transition-all duration-300;
}

/* Enhanced dropdown items */
.hover\:bg-white\/30 {
    @apply hover:bg-white/20
           active:bg-white/25
           transition-all duration-200;
}

/* Shiny file upload card */
.bg-white\/20 {
    @apply bg-gradient-to-br from-white/25 to-black/15
           hover:from-white/30 hover:to-black/20
           shadow-[0_8px_32px_0_rgba(31,38,135,0.2)];
}

/* Add subtle shine to buttons */
button {
    @apply relative overflow-hidden
           after:absolute after:inset-0 
           after:bg-gradient-to-t after:from-transparent after:to-white/10
           after:opacity-0 after:hover:opacity-100
           after:transition-opacity after:duration-300;
}

/* Add subtle light reflection */
.sidebar-shine {
    @apply after:absolute after:inset-0 
           after:bg-gradient-to-br after:from-white/5 after:to-transparent
           after:pointer-events-none;
}

/* Add responsive breakpoints */
@media (max-width: 640px) {
    .sidebar-open {
        transform: translateX(0);
    }
}

/* Remove any initial backgrounds from links */
.nav-item, 
.dropdown-item {
    @apply bg-transparent;
}

/* Update hover and active states */
.hover\:bg-white\/30 {
    @apply hover:bg-white/20
           active:bg-white/25
           transition-all duration-200;
}

/* Update dropdown items */
.pl-8 a {
    @apply hover:bg-white/20
           active:bg-white/25
           transition-all duration-200;
}

/* Keep the glass effect for the sidebar container */
.glass-effect {
    @apply bg-gradient-to-br from-white/20 to-black/15
           backdrop-filter backdrop-blur-xl 
           border border-white/20
           shadow-[0_4px_30px_rgba(0,0,0,0.15)]
           after:absolute after:inset-0 
           after:bg-gradient-to-t after:from-transparent after:to-white/5
           after:pointer-events-none;
}

/* Remove any default backgrounds */
[class*="bg-"] {
    @apply bg-transparent;
}

/* Only apply backgrounds on hover/active states */
[class*="hover\:bg-"],
[class*="active\:bg-"] {
    @apply transition-all duration-200;
}

/* Remove existing hover states and add new ones */
.nav-item, 
.dropdown-item {
    @apply bg-transparent;
}

/* Update top-level menu items */
.flex.px-4.py-2.hover\:text-purple-800 {
    @apply hover:shadow-[0_0_15px_rgba(107,33,168,0.15)]
           transition-all duration-200 ease-in-out;
}

/* Add active state for clicked items */
.flex.px-4.py-2.hover\:text-purple-800.active {
    @apply shadow-[0_0_20px_rgba(107,33,168,0.2)]
           text-purple-800;
}

/* Remove default hover backgrounds */
.hover\:bg-white\/30 {
    @apply hover:bg-transparent;
}

/* Update dropdown items */
.pl-8 a {
    @apply hover:bg-transparent
           hover:shadow-[0_0_10px_rgba(107,33,168,0.1)]
           active:shadow-[0_0_15px_rgba(107,33,168,0.15)]
           transition-all duration-200;
}

/* Keep other existing styles ... */
</style>