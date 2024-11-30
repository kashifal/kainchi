<template lang="">
     <div class="w-full max-w-6xl bg-white shadow-lg rounded-lg overflow-hidden">
    <!-- Header Navigation -->
    <div class="px-6 py-4 border-b">
      <nav class="text-sm text-gray-600">
        <span class="hover:underline cursor-pointer">Dashboard</span>
        <span class="mx-2">></span>
        <span class="hover:underline cursor-pointer">Categories</span>
        <span class="mx-2">></span>
        <span class="font-semibold text-gray-800">New</span>
      </nav>
    </div>

    <!-- Content Section -->
    <div class="flex flex-col md:flex-row">
      <!-- Left Section -->
      <div class="w-full md:w-2/3 p-8">
        <div class="flex flex-col items-center justify-center h-64 bg-gray-100 rounded-lg">
          <div class="bg-gray-300 p-10 rounded-full">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-20 w-20 text-gray-400" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3 7h18M3 12h18m-9 5h9"></path>
            </svg>
          </div>
        </div>
        <div class="mt-8 border-2 rounded-2xl p-2">
          <h2 class="text-2xl font-semibold text-gray-800">Understanding various Categories in Kain'chi</h2>
          <p class="mt-2 text-sm text-gray-600 leading-relaxed">
            Fusce at nisi eget dolor rhoncus facilisis. Mauris ante nisi, consectetur at luctus et, porta ut dolor. Cras vehicula, mauris nec ultricies efficitur, nulla urna pharetra diam, sit amet eleifend erat orci vitae metus. Nulla eu consectetur ipsum.
          </p>
        </div>
      </div>

      <!-- Right Section -->
      <div class="w-full md:w-1/3  p-8">
        <h3 class="text-lg font-semibold text-gray-700">Categories and Subcategories</h3>
        <div class="mt-4 flex items-center space-x-6">
          <!-- Radio Buttons -->
          <div class="flex items-center">
           <div class="flex items-center justify-center bg-gray-100">
  <label for="toggle" class="relative cursor-pointer">
    <input type="checkbox" id="toggle" class="sr-only peer" />
    <div class="w-11 h-6 bg-gray-300 rounded-full peer-checked:bg-indigo-700 peer-focus:ring-2 peer-focus:ring-indigo-300 transition-all"></div>
    <div
      class="w-5 h-5 bg-white rounded-full shadow-md absolute top-0.5 left-0.5 peer-checked:translate-x-6 transition-all"
    ></div>
  </label>
</div>
            <label for="category" class="ml-1 text-sm text-gray-700">Category</label>
          </div>
          <div class="flex items-center">
           <div class="flex items-center justify-center bg-gray-100">
  <label for="tooggle" class="relative cursor-pointer">
    <input type="checkbox" id="tooggle" class="sr-only peer" />
    <div class="w-11 h-6 bg-gray-300 rounded-full peer-checked:bg-indigo-700 peer-focus:ring-2 peer-focus:ring-indigo-300 transition-all"></div>
    <div
      class="w-5 h-5 bg-white rounded-full shadow-md absolute top-0.5 left-0.5 peer-checked:translate-x-6 transition-all"
    ></div>
  </label>
</div>
            <label for="subcategory" class="ml-2 text-sm text-gray-700">Subcategory</label>
          </div>
        </div>

        <!-- Form -->
        <form class="mt-6 space-y-4">
          <div>
            <label for="name" class="block text-sm font-medium text-gray-700">Name</label>
            <input type="text" id="name" name="name" class="mt-1 py-2 bg-gray-100 block w-full border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
          </div>
          <div>
            <label for="keywords" class="block text-sm font-medium text-gray-700">Keywords</label>
            <input type="text" id="keywords" name="keywords" class="mt-1 py-2 bg-gray-100 bg-gray-100block w-full border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
          </div>
          <div>
            <label for="additional-keywords" class="block text-sm font-medium text-gray-700">Additional Keywords</label>
            <input type="text" id="additional-keywords" name="additional-keywords" class="mt-1 block w-full  py-2 bg-gray-100 border border-gray-300 rounded-md shadow-sm focus:ring-purple-500 focus:border-purple-500">
          </div>
          <p class="text-xs text-gray-500">Note: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed diam nonummy.</p>
          <button type="submit" class="w-full py-2 bg-indigo-700 text-white rounded-full shadow-md hover:bg-indigo-600 focus:outline-none focus:ring-2 focus:ring-purple-500 focus:ring-offset-1">
            Create
          </button>
        </form>
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