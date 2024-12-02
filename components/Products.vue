<template lang="">
    <div class="pb-4 mb-6 ">
      <nav class="text-sm text-gray-600">
        <span class="cursor-pointer hover:underline">Dashboard</span>
        <span class="mx-2">></span>
        <span class="cursor-pointer hover:underline">Products</span>
        <span class="mx-2">></span>
        <span class="font-semibold text-gray-800">New</span>
      </nav>
    </div>
    <h1 class="text-2xl xl:text-[36px] mr-7 xl:mb-0 font-semibold">Products</h1>

<div class="flex flex-col gap-5 xl:flex-row mt-10">

  <!-- Main Container -->
  <div class="w-full max-w-full p-6 md:p-10 bg-white rounded-3xl shadow-lg">
    <!-- Header Navigation -->
    

    <!-- Form Section -->
    <div class="flex flex-col space-y-8 text-[#212121] md:flex-row md:space-y-0 md:space-x-8">
      <!-- Left Section -->
      <div class="w-full ">
        <div>
         <div class="flex items-center justify-between" :class="{'mb-4': isProductSectionOpen}" @click="toggleProductSection">
          <h3 class="text-lg xl:text-[26px] font-medium">Product Name</h3>
          <svg :class="['size-6 cursor-pointer transition-transform duration-300', isProductSectionOpen ? '' : 'rotate-180']" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16"><path fill="currentColor" d="m2.931 10.843l4.685-4.611a.546.546 0 0 1 .768 0l4.685 4.61a.55.55 0 0 0 .771 0a.53.53 0 0 0 0-.759l-4.684-4.61a1.65 1.65 0 0 0-2.312 0l-4.684 4.61a.53.53 0 0 0 0 .76a.55.55 0 0 0 .771 0"/></svg>
          </div> 

          <transition
            enter-active-class="transition-all duration-300 ease-out"
            leave-active-class="transition-all duration-300 ease-in"
            enter-from-class="transform opacity-0 max-h-0"
            enter-to-class="transform opacity-100 max-h-[1000px]"
            leave-from-class="transform opacity-100 max-h-[1000px]"
            leave-to-class="transform opacity-0 max-h-0"
          >
            <div class="space-y-6 mt-6 overflow-hidden" v-show="isProductSectionOpen">
              <!-- Title -->
              <div>
                <label for="title" class="block text-sm lg:text-[18px] font-medium text-[#656565]">Title</label>
                <input type="text" id="title" name="title" class="w-full px-4 py-4 bg-[#DBDBDB] shadow-[0px_0px_6px_#0000001A] mt-2 blur-[8px] brightness-[-5px] border rounded-md border-[#DBDBDB]  mt-[6px]">
                <p class="mt-1 text-xs text-[#A988F5] justify-end flex items-center gap-2">
                  <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 21 21"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M17 4a2.12 2.12 0 0 1 0 3l-9.5 9.5l-4 1l1-3.944l9.504-9.552a2.116 2.116 0 0 1 2.864-.125zM9.5 17.5h8m-2-11l1 1"/></svg>
                  0/20 - 70</p>
              </div>
              <!-- Subtitle -->
              <div>
                <label for="title" class="block text-sm lg:text-[18px] font-medium text-[#656565]">Sub Title</label>
                <input type="text" id="title" name="title" class="w-full px-4 py-4 bg-[#DBDBDB] shadow-[0px_0px_6px_#0000001A] mt-2 blur-[8px] brightness-[-5px] border rounded-md border-[#DBDBDB]  mt-[6px]">
                <p class="mt-1 text-xs text-[#A988F5] justify-end flex items-center gap-2">
                  <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 21 21"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M17 4a2.12 2.12 0 0 1 0 3l-9.5 9.5l-4 1l1-3.944l9.504-9.552a2.116 2.116 0 0 1 2.864-.125zM9.5 17.5h8m-2-11l1 1"/></svg>
                  0/20 - 70</p>
              </div>
              <!-- Short Description -->
              <div>
                <label for="short-description" class="block text-sm lg:text-[18px] font-medium text-[#656565]">Short description</label>
                <textarea id="short-description" name="short-description" rows="4" class="w-full px-4 py-4 bg-[#DBDBDB] shadow-[0px_0px_6px_#0000001A] mt-2 blur-[8px] brightness-[-5px] border rounded-md border-[#DBDBDB]  mt-[6px]"></textarea>
               <div class="flex items-center justify-between">
                <p class="mt-1 text-xs text-purple-500">Your short description tag should be between 100-160 characters</p>
                <p class="mt-1 text-xs text-[#A988F5] justify-end flex items-center gap-2">
                  <svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="21" height="21" viewBox="0 0 21 21"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M17 4a2.12 2.12 0 0 1 0 3l-9.5 9.5l-4 1l1-3.944l9.504-9.552a2.116 2.116 0 0 1 2.864-.125zM9.5 17.5h8m-2-11l1 1"/></svg>
                  0/20 - 70</p> 
              </div>
              </div>
            </div>
          </transition>
        </div>
      </div>

      <!-- Right Section -->
    
    </div>
  </div>

    <div class="w-full space-y-3 text-[#212121] xl:w-1/3">
        <!-- Availability -->
        <div class="p-5 bg-white border border-gray-300 rounded-3xl">
          <h3 class="text-lg font-medium text-gray-700">Availability</h3>
          <select id="availability" name="availability" class="block w-full py-2 px-2 mt-4 bg-gray-100 border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
            <option>Available</option>
            <option>Unavailable</option>
          </select>
        </div>

        <!-- Pricing -->
        <div class="p-5 bg-white border  border-gray-300 rounded-3xl">
          <h3 class="text-lg font-medium xl:text-[22px] text-gray-700">Pricing</h3>
          <p class="mt-1 text-sm text-gray-400">Add a reasonable price</p>
          <div class="mt-4 space-y-4">
            <!-- Price -->
            <div>
              <label for="price" class="block text-sm font-medium text-gray-700">Price</label>
              <div class="relative mt-1">
                <span class="absolute inset-y-0 left-0 flex items-center px-4 pl-4 text-center text-white bg-[#A988F5] rounded-lg">$</span>
                <input type="number" id="price" name="price" class="block w-full py-2 pl-10 bg-gray-100  rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              </div>
            </div>
            <!-- Old Price -->
            <div>
              <label for="old-price" class="block text-sm font-medium text-gray-700">Old price</label>
              <div class="relative mt-1">
                <span class="absolute inset-y-0 left-0 flex items-center px-4 pl-4 text-center text-white bg-[#A988F5] rounded-lg">$</span>
                <input type="number" id="old-price" name="old-price" class="block w-full py-2 pl-10 bg-gray-100  rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              </div>
            </div>
            <!-- Compare to Price -->
            <div class="flex items-start space-x-2">
              <svg class="text-[#3A0CA3]" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2L9.19 8.63L2 9.24l5.46 4.73L5.82 21z"/></svg>
              <div>
                <label for="compare-price" class="text-sm font-medium text-gray-700">Set "Compare to" price</label>
                <p class="text-xs text-gray-400">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
              </div>
            </div>
            <!-- Cost Per Item -->
            <div>
              <label for="cost-per-item" class="block text-sm font-medium text-gray-700">Cost per item</label>
              <div class="relative mt-1">
                <span class="absolute inset-y-0 left-0 flex items-center px-4 pl-4 text-center text-white bg-[#A988F5] rounded-lg">$</span>
                <input type="number" id="cost-per-item" name="cost-per-item" class="block w-full py-2 pl-10 bg-gray-100  rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              </div>
              <p class="mt-1 text-xs text-gray-400">Customers won’t see this</p>
            </div>
          </div>
        </div>
      </div>
</div>


</template>
<script>
export default {
  data() {
    return {
      isProductSectionOpen: true
    }
  },
  methods: {
    toggleProductSection() {
      this.isProductSectionOpen = !this.isProductSectionOpen
    }
  }
}
</script>
<style lang="">
    
</style>