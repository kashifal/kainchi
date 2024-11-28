<template lang="">
     <header class="bg-[#D1D1D6] py-[20px]">
        <div class="bg-[#D1D1D6] text-white flex items-center p-4 w-[95%] rounded-2xl mx-auto shadow-lg">

            <div class="flex items-center space-x-4">
              
              <img src="./tdesign--letters-k white.svg" class="h-[50px]" alt="Logo">
              
              <span class="text-2xl font-bold mt-[4px]">Kainchi</span>
            </div>
          
            
            <div class="flex items-center flex-grow ml-8 relative">
              <div class="relative w-full max-w-4xl ml-[100px]">
                <input type="text" class="w-full py-2 pl-10 pr-20 rounded-full bg-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-purple-500" placeholder="Search...">
                <img src="./si--search-line.svg" class="absolute top-[25%] left-3 h-5" alt="Search Icon">
                <div class="border-l-[2px] border-black">
                    <span class="absolute right-10 top-1/2 transform -translate-y-1/2 text-gray-400 text-sm ">Filter</span>
                    <img src="./mdi--keyboard-arrow-down.svg" class="absolute right-3 top-1/2 transform -translate-y-1/2 h-4" alt="Dropdown Icon">
                </div>
              </div>
            </div>
          
            
            <div class="flex items-center space-x-8 mr-[50px]">
              <img src="" class="h-6 cursor-pointer" alt="Messages Icon">
              <img src="" class="h-6 cursor-pointer" alt="Settings Icon">
              <img src="" class="h-10 w-10 rounded-full" alt="User Avatar">
            </div>
        </div>
    </header>
</template>
<script>
export default {
    
}
</script>
<style lang="">
    
</style>