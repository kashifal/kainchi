<template lang="">
    <div>
        <main class="flex-1 px-6 pt-2 rounded-lg ">
            
            <header class="mb-8">
                <p class="text-sm text-gray-600">Dashboard > Profiles > New</p>
                <h1 class="mt-2 text-2xl font-bold text-gray-700">Products</h1>
            </header>
        
            <div class="flex-1 bg-[#F0F0F2] rounded-lg shadow-lg p-6">
                <h2 class="mb-6 text-xl font-bold text-gray-700">Products Name</h2>
          
                <!-- Form -->
                <form class="grid grid-cols-1 gap-6 md:grid-cols-12 ">
                  <!-- Left Section -->
                  <div class="col-span-8 ">
                    <div class="mb-4 ">
                      <label for="title" class="block text-gray-600 font-semibold text-[14px] ">Title</label>
                      <input type="text" id="title" placeholder="" class="w-full px-4 py-3 border bg-[#E8EAEB] mt-[10px] shadow-md rounded-md focus:outline-none focus:ring focus:ring-indigo-200">
                      <div class="flex justify-end mt-[4px] text-[12px] text-[#BAA0F6]">
                        <img src="./bxs--pencil.svg" class="h-[14px] mr-[6px] mt-[2px]" alt="">
                        <p class="font-semibold">0/20 - 70</p>
                    </div>
                    </div>
                    <div class="mb-4 ">
                        <label for="title" class="block text-gray-600 font-semibold text-[14px] ">Sub Title</label>
                        <input type="text" id="title" placeholder="" class="w-full px-4 py-3 border bg-[#E8EAEB] mt-[10px] shadow-md rounded-md focus:outline-none focus:ring focus:ring-indigo-200">
                        <div class="flex justify-end mt-[4px] text-[12px] text-[#BAA0F6]">
                            <img src="./bxs--pencil.svg" class="h-[14px] mr-[6px] mt-[2px]" alt="">
                            <p class="font-semibold">0/20 - 70</p>
                        </div>
                      </div>
                    <div>
                        <div class="mb-4 ">
                            <label for="title" class="block text-gray-600 font-semibold text-[14px] ">Sub Title</label>
                            <input type="text" id="title" placeholder="" class="w-full px-4 py-14 border bg-[#E8EAEB] mt-[10px] shadow-md rounded-md focus:outline-none focus:ring focus:ring-indigo-200">
                          </div>
                        <div>
                  </div>
                    </div>
                    <div class="flex justify-between text-[#BAA0F6] text-[12px]">
                        <p>Your short description tag should be between 100-160 characters</p>
                        <div class="flex">
                            <img src="./bxs--pencil.svg" class="h-[14px] mr-[6px] mt-[2px]" alt="">
                            <p>0/20 - 70</p>
                        </div>

                    </div>
                  </div>
          
                  <!-- Right Section -->
                  <div class="col-span-4">
                    <div class="mb-4 bg-[#F1F1F9] px-4 py-6 rounded-2xl">
                      <label for="availability" class="block text-gray-600 font-bold text-[14px]">Availability</label>
                      <select id="availability" class="w-full px-4 py-2 border rounded-md bg-[#E4E4EC] text-[12px] mt-[6px] tracking-wide text-[#A1A0A3] focus:outline-none focus:ring focus:ring-indigo-200">
                        <option>Available</option>
                        <option>Out of Stock</option>
                      </select>
                    </div>
                    <div class="border-t mt-6 pt-4 bg-[#F1F1F9] rounded-2xl px-4 ">
                      <h3 class="font-bold text-[1.1rem] tracking-wide">Pricing</h3>
                      <p class="text-[12px] text-[#A1A0A3] ">Add a reasonable price</p>
                      <div class="mb-4  mt-[10px]">
                        <label for="price" class="block text-gray-600 font-medium tracking-wide text-[13px]">Price</label>
                        <div class="flex bg-[#E5E5ED] rounded-lg mt-[6px]">
                            <img src="./carbon--currency-dollar.svg" class="bg-[#A988F5] w-[35px] " alt="">
                        <input type="text" id="price" placeholder="0.00" class="w-full px-4 py-2 bg-transparent rounded-md focus:outline-none focus:ring focus:ring-indigo-200">
                    </div>
                      </div>
                      <div class="mb-4  mt-[10px]">
                        <label for="price" class="block text-gray-600 font-medium tracking-wide text-[13px]">Old price</label>
                        <div class="flex bg-[#E5E5ED] rounded-lg mt-[6px]">
                            <img src="./carbon--currency-dollar.svg" class="bg-[#A988F5] w-[35px] " alt="">
                        <input type="text" id="price" placeholder="0.00" class="w-full px-4 py-2 bg-transparent rounded-md focus:outline-none focus:ring focus:ring-indigo-200">
                    </div>
                      </div>
                      <div class="flex">
                        <img src="./ic--baseline-star.svg" class="h-[18px]" alt="">
                        <p class="text-[12px] font-semibold text-[#656565] ml-[10px]">Set "Compare to" price</p>
                      </div>
                      <p class="text-[11px] mt-[10px] text-[#656565]">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptates, aut ipsum? Similique</p>


                      <div class="mb-4  mt-[10px]">
                        <label for="price" class="block text-gray-600 font-medium tracking-wide text-[13px]">Cost per item</label>
                        <div class="flex bg-[#E5E5ED] rounded-lg mt-[6px]">
                            <img src="./carbon--currency-dollar.svg" class="bg-[#A988F5] w-[35px] " alt="">
                        <input type="text" id="price" placeholder="0.00" class="w-full px-4 py-2 bg-transparent rounded-md focus:outline-none focus:ring focus:ring-indigo-200">
                    </div>
                      </div>
                    </div>
                  </div>
                </form>
              </div>
           
        </main>
    </div>
</template>
<script>
export default {
    
}
</script>
<style lang="">
    
</style>