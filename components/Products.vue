<template lang="">
    

<div class="flex xl:flex-row flex-col gap-5">
  <!-- Main Container -->
  <div class="w-full max-w-full bg-white shadow-lg rounded-lg p-5">
    <!-- Header Navigation -->
    <div class="border-b pb-4 mb-6">
      <nav class="text-sm text-gray-600">
        <span class="hover:underline cursor-pointer">Dashboard</span>
        <span class="mx-2">></span>
        <span class="hover:underline cursor-pointer">Products</span>
        <span class="mx-2">></span>
        <span class="font-semibold text-gray-800">New</span>
      </nav>
      <h1 class="text-2xl font-semibold text-gray-800 mt-2">Products</h1>
    </div>

    <!-- Form Section -->
    <div class="flex flex-col md:flex-row space-y-8 md:space-y-0 md:space-x-8">
      <!-- Left Section -->
      <div class="w-full ">
        <div>
          <h3 class="text-lg font-medium text-gray-700 mb-4">Product Name</h3>
          <div class="space-y-6">
            <!-- Title -->
            <div>
              <label for="title" class="block  text-sm font-medium text-gray-700">Title</label>
              <input type="text" id="title" name="title" class="mt-1 py-2 bg-gray-100 block w-full border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              <p class="text-xs text-gray-400 mt-1">0/20 - 70</p>
            </div>
            <!-- Subtitle -->
            <div>
              <label for="subtitle" class="block text-sm font-medium text-gray-700">Sub Title</label>
              <input type="text" id="subtitle" name="subtitle" class="mt-1 py-2 bg-gray-100 block w-full border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              <p class="text-xs text-gray-400 mt-1">0/20 - 70</p>
            </div>
            <!-- Short Description -->
            <div>
              <label for="short-description" class="block text-sm font-medium text-gray-700">Short description</label>
              <textarea id="short-description" name="short-description" rows="4" class="mt-1 py-2 bg-gray-100 block w-full border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500"></textarea>
              <p class="text-xs text-purple-500 mt-1">Your short description tag should be between 100-160 characters</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Right Section -->
    
    </div>
  </div>

    <div class="w-full xl:w-1/3 space-y-8">
        <!-- Availability -->
        <div class="bg-white border border-gray-300 rounded-xl p-4">
          <h3 class="text-lg font-medium text-gray-700">Availability</h3>
          <select id="availability" name="availability" class="mt-4 py-2 bg-gray-100 block w-full border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
            <option>Available</option>
            <option>Unavailable</option>
          </select>
        </div>

        <!-- Pricing -->
        <div class="bg-white border border-gray-300 rounded-xl p-4">
          <h3 class="text-lg font-medium text-gray-700">Pricing</h3>
          <p class="text-sm text-gray-400 mt-1">Add a reasonable price</p>
          <div class="space-y-4 mt-4">
            <!-- Price -->
            <div>
              <label for="price" class="block text-sm font-medium text-gray-700">Price</label>
              <div class="relative mt-1">
                <span class="absolute inset-y-0 left-0 flex items-center text-center pl-4 text-white bg-indigo-700 px-4 rounded-lg">$</span>
                <input type="number" id="price" name="price" class="pl-10 py-2 bg-gray-100 block w-full border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              </div>
            </div>
            <!-- Old Price -->
            <div>
              <label for="old-price" class="block text-sm font-medium text-gray-700">Old price</label>
              <div class="relative mt-1">
                <span class="absolute inset-y-0 left-0 flex items-center text-center pl-4 text-white bg-indigo-700 px-4 rounded-lg">$</span>
                <input type="number" id="old-price" name="old-price" class="pl-10 py-2 bg-gray-100 block w-full border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              </div>
            </div>
            <!-- Compare to Price -->
            <div class="flex items-start space-x-2">
              <input type="checkbox" id="compare-price" name="compare-price" class="h-5 w-5 text-purple-600 focus:ring-purple-500 border-gray-300">
              <div>
                <label for="compare-price" class="text-sm font-medium text-gray-700">Set "Compare to" price</label>
                <p class="text-xs text-gray-400">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
              </div>
            </div>
            <!-- Cost Per Item -->
            <div>
              <label for="cost-per-item" class="block text-sm font-medium text-gray-700">Cost per item</label>
              <div class="relative mt-1">
                <span class="absolute inset-y-0 left-0 flex items-center text-center pl-4 text-white bg-indigo-700 px-4 rounded-lg">$</span>
                <input type="number" id="cost-per-item" name="cost-per-item" class="pl-10 block py-2 bg-gray-100 w-full border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              </div>
              <p class="text-xs text-gray-400 mt-1">Customers won’t see this</p>
            </div>
          </div>
        </div>
      </div>
</div>


</template>
<script>
export default {
    
}
</script>
<style lang="">
    
</style>