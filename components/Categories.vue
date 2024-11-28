<template lang="">
     <main class="flex-1 p-8">
            <!-- Header -->
            <header class="flex items-center justify-between mb-8">
              <h1 class="text-2xl font-semibold text-gray-700">Categories</h1>
            </header>
        
            <!-- Content Section -->
            <div class="flex space-x-8 bg-white">
              <!-- Left Section -->
              <div class="flex-1">
                <div class="w-[100%] flex justify-center mt-[240px]">
                    <img src="./ci--image-02.svg" class="h-[40px]" alt="">
                </div>
                <div class="mt-[100px] p-4 rounded-lg border-2 ml-[20px]">
                    <p class="font-bold text-[1.3rem]">Understanding various categories in Kainchi</p>
                    <p class="text-[12px] text-gray-600 mt-[10px]">
                        Lorem ipsum dolor sit amet, consectetur<br>
                        amet consectetur adipisicing elit. Veniam non velit obcaecati <br>
                        amet consectetur adipisicing elit. Veniam non velit obcaecati <br>
                        amet consectetur adipisicing elit. Veniam non velit obcaecati <br>
                        dolor incidunt praesentium dolor! Recusandae impedi
                    </p>
                </div>
            </div>
        
              <!-- Right Section -->
              <div class="w-1/2  p-6">
                <h2 class="text-[1.7rem] font-semibold text-gray-700 mb-4">Categories and subcategories</h2>
                <form class="space-y-4">
                  <!-- Toggle Button -->
                  <div class="flex items-center space-x-4">
                    <span class="text-sm text-gray-700 font-bold">Category</span>
                    <label for="toggle" class="relative inline-block w-12 h-6">
                      <input
                        type="checkbox"
                        id="toggle"
                        class="peer hidden"
                      />
                      <span
                        class="absolute cursor-pointer inset-0 bg-gray-300 rounded-full transition-all duration-300 peer-checked:bg-indigo-500"
                      ></span>
                      <span
                        class="absolute left-1 top-1 w-4 h-4 bg-white rounded-full transition-all duration-300 peer-checked:translate-x-6"
                      ></span>
                    </label>
                    <span class="text-sm text-gray-700 font-bold">Subcategory</span>
                    <label for="toggle" class="relative inline-block w-12 h-6">
                        <input
                          type="checkbox"
                          id="toggle"
                          class="peer hidden"
                        />
                        <span
                          class="absolute cursor-pointer inset-0 bg-gray-300 rounded-full transition-all duration-300 peer-checked:bg-indigo-500"
                        ></span>
                        <span
                          class="absolute left-1 top-1 w-4 h-4 bg-white rounded-full transition-all duration-300 peer-checked:translate-x-6"
                        ></span>
                      </label>
                  </div>
        
                  <!-- Name Input -->
                  <div>
                    <label for="name" class="block text-sm font-semibold text-gray-700">Name</label>
                    <input
                      type="text"
                      id="name"
                      class="w-full px-4 mt-[6px] py-4 border rounded-md bg-white focus:outline-none focus:ring focus:ring-indigo-300 bg-gradient-to-r from-purple-100 to-purple-200 shadow-md rounded-lg"
                      placeholder=""
                    />
                  </div>
        
                  <!-- Keywords Input -->
                  <div>
                    <label for="name" class="block text-sm font-semibold text-gray-700">Keywords</label>
                    <input
                      type="text"
                      id="name"
                      class="w-full px-4 mt-[6px] py-5 border rounded-md bg-white focus:outline-none focus:ring focus:ring-indigo-300 bg-gradient-to-r from-purple-100 to-purple-200 shadow-md rounded-lg"
                      placeholder=""
                    />
                  </div>

                  <div>
                    <label for="name" class="block text-sm font-semibold text-gray-700">Keywords</label>
                    <input
                      type="text"
                      id="name"
                      class="w-full px-4 mt-[6px] py-7 border rounded-md bg-white focus:outline-none focus:ring focus:ring-indigo-300 bg-gradient-to-r from-purple-100 to-purple-200 shadow-md rounded-lg"
                      placeholder=""
                    />
                  </div>
        
                  <!-- Note -->
                   <div class="flex">
                    <p class="rounded-full bg-[#A988F5] text-[white] px-[20px] text-[12px] font-bold h-[26px] pt-[3px]">Note</p>
                  <p class="text-xs text-gray-500 ml-[10px] font-medium">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonumy elitr...
                  </p>
                </div>
                  <!-- Submit Button -->
                  <button
                    type="submit"
                    class="w-full bg-indigo-600 text-white py-4 rounded-full hover:bg-indigo-500"
                  >
                    Create
                  </button>
                </form>
              </div>
            </div>
          </main>
</template>
<script>
export default {
    
}
</script>
<style lang="">
    
</style>