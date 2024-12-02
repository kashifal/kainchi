<template lang="">
    

<div class="flex flex-col gap-5 xl:flex-row">
  <!-- Main Container -->
  <div class="w-full max-w-full p-5 bg-white rounded-lg shadow-lg">
    <!-- Header Navigation -->
    <div class="pb-4 mb-6 border-b">
      <nav class="text-sm text-gray-600">
        <span class="cursor-pointer hover:underline">Dashboard</span>
        <span class="mx-2">></span>
        <span class="cursor-pointer hover:underline">Products</span>
        <span class="mx-2">></span>
        <span class="font-semibold text-gray-800">New</span>
      </nav>
      <h1 class="mt-2 text-2xl font-semibold text-gray-800">Products</h1>
    </div>

    <!-- Form Section -->
    <div class="flex flex-col space-y-8 md:flex-row md:space-y-0 md:space-x-8">
      <!-- Left Section -->
      <div class="w-full ">
        <div>
          <h3 class="mb-4 text-lg font-medium text-gray-700">Product Name</h3>
          <div class="space-y-6">
            <!-- Title -->
            <div>
              <label for="title" class="block text-sm font-medium text-gray-700">Title</label>
              <input type="text" id="title" name="title" class="block w-full py-2 mt-1 bg-gray-100 border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              <p class="mt-1 text-xs text-gray-400">0/20 - 70</p>
            </div>
            <!-- Subtitle -->
            <div>
              <label for="subtitle" class="block text-sm font-medium text-gray-700">Sub Title</label>
              <input type="text" id="subtitle" name="subtitle" class="block w-full py-2 mt-1 bg-gray-100 border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              <p class="mt-1 text-xs text-gray-400">0/20 - 70</p>
            </div>
            <!-- Short Description -->
            <div>
              <label for="short-description" class="block text-sm font-medium text-gray-700">Short description</label>
              <textarea id="short-description" name="short-description" rows="4" class="block w-full py-2 mt-1 bg-gray-100 border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500"></textarea>
              <p class="mt-1 text-xs text-purple-500">Your short description tag should be between 100-160 characters</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Right Section -->
    
    </div>
  </div>

    <div class="w-full space-y-8 xl:w-1/3">
        <!-- Availability -->
        <div class="p-4 bg-white border border-gray-300 rounded-xl">
          <h3 class="text-lg font-medium text-gray-700">Availability</h3>
          <select id="availability" name="availability" class="block w-full py-2 mt-4 bg-gray-100 border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
            <option>Available</option>
            <option>Unavailable</option>
          </select>
        </div>

        <!-- Pricing -->
        <div class="p-4 bg-white border border-gray-300 rounded-xl">
          <h3 class="text-lg font-medium text-gray-700">Pricing</h3>
          <p class="mt-1 text-sm text-gray-400">Add a reasonable price</p>
          <div class="mt-4 space-y-4">
            <!-- Price -->
            <div>
              <label for="price" class="block text-sm font-medium text-gray-700">Price</label>
              <div class="relative mt-1">
                <span class="absolute inset-y-0 left-0 flex items-center px-4 pl-4 text-center text-white bg-indigo-700 rounded-lg">$</span>
                <input type="number" id="price" name="price" class="block w-full py-2 pl-10 bg-gray-100 border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              </div>
            </div>
            <!-- Old Price -->
            <div>
              <label for="old-price" class="block text-sm font-medium text-gray-700">Old price</label>
              <div class="relative mt-1">
                <span class="absolute inset-y-0 left-0 flex items-center px-4 pl-4 text-center text-white bg-indigo-700 rounded-lg">$</span>
                <input type="number" id="old-price" name="old-price" class="block w-full py-2 pl-10 bg-gray-100 border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
              </div>
            </div>
            <!-- Compare to Price -->
            <div class="flex items-start space-x-2">
              <input type="checkbox" id="compare-price" name="compare-price" class="w-5 h-5 text-purple-600 border-gray-300 focus:ring-purple-500">
              <div>
                <label for="compare-price" class="text-sm font-medium text-gray-700">Set "Compare to" price</label>
                <p class="text-xs text-gray-400">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
              </div>
            </div>
            <!-- Cost Per Item -->
            <div>
              <label for="cost-per-item" class="block text-sm font-medium text-gray-700">Cost per item</label>
              <div class="relative mt-1">
                <span class="absolute inset-y-0 left-0 flex items-center px-4 pl-4 text-center text-white bg-indigo-700 rounded-lg">$</span>
                <input type="number" id="cost-per-item" name="cost-per-item" class="block w-full py-2 pl-10 bg-gray-100 border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
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
    
}
</script>
<style lang="">
    
</style>