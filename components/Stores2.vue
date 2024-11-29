<template lang="">
      <main class="flex-1 p-8">
            <header class="flex items-center">
                <h1 class="text-2xl font-semibold text-gray-700">Stores</h1>

                <!-- Number Line Section -->
                <div class="flex items-center justify-around w-full ">
                    <div
                        class="flex items-center justify-center w-10 h-10 font-bold text-white bg-indigo-500 rounded-full">
                        1</div>
                    <div class="w-40 h-2 bg-indigo-500"></div>
                    <div class="flex items-center justify-center w-10 h-10 font-bold text-white bg-indigo-500 rounded-full">2
                    </div>
                    <div class="w-40 h-2 bg-white"></div>
                    <div class="flex items-center justify-center w-10 h-10 font-bold text-black bg-white rounded-full">
                        3</div>
                    <div class="w-40 h-2 bg-white"></div>
                    <div class="flex items-center justify-center w-10 h-10 font-bold text-black bg-white rounded-full">4
                    </div>
                </div>
            </header>

        
            <div class="p-8 mt-8 bg-white rounded-md shadow">
                
              
        
                <!-- Flex Layout for Form and Supporting Section -->
                <div class="flex space-x-8">
                    <!-- Supporting Section -->
                    <div class="flex flex-col justify-between w-1/2 p-6 rounded-md bg-gray-50">
                        <div class="w-[100%] flex justify-center mt-[170px]">
                            <!-- <img src="./ci--image-02.svg" class="h-[40px]" alt=""> -->

                        </div>
                        <div class="mt-[100px] p-4  rounded-lg border-2 ">
                            <p class="font-semibold text-[1.3rem]">Bring more traffic to your store - even in real life</p>
                            <p class="text-[12px] text-gray-600">Lorem ipsum dolor sit amet, consectetur<br> amet consectetur adipisicing elit. Veniam non velit obcaecati <br> dolor incidunt praesentium dolor! Recusandae impedi </p>
                            
                        </div>
                    </div>
        
                    <!-- Form Section -->
                    <div class="w-1/2">
                        <h2 class="text-lg font-bold text-gray-700">Add a company address to get paid and set up delivery.</h2>
                        <p class="text-[12px] text-gray-500 ">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonumy...
                        </p>
        
                        <form class="mt-6">
                            <div class="space-y-4">
                                <div>
                                    <label class="block text-gray-700 font-bold tracking-wider text-[14px]">What's your store address? - State / Province</label>
                                    <input type="text" class="w-full px-4 py-3 bg-gray-100 border rounded-md focus:outline-none focus:ring focus:ring-indigo-300">
                                </div>
                                <div>
                                    <label class="block text-gray-700 font-bold tracking-wider text-[14px]">What's your store address? - City</label>
                                    <input type="text" class="w-full px-4 py-3 bg-gray-100 border rounded-md focus:outline-none focus:ring focus:ring-indigo-300">
                                </div>
                                <div>
                                    <label class="block text-gray-700 font-bold tracking-wider text-[14px]">What's your store address? - Zip Code</label>
                                    <input type="text" class="w-full px-4 py-3 bg-gray-100 border rounded-md focus:outline-none focus:ring focus:ring-indigo-300">
                                </div>
                            </div>
                        </form>
                        <div class="flex justify-between mt-8">
                            <button class="bg-gray-200 text-gray-700 px-6 py-2 hover:bg-gray-300 w-[30%] rounded-full ">Previous</button>
                            <button class="bg-indigo-600 text-white px-6 py-2 hover:bg-indigo-500 w-[60%] rounded-full ">Next</button>
                        </div>
                    </div>
                </div>
        
                <!-- Buttons -->
                
            </div>
        </main>
</template>
<script>
export default {
    
}
</script>
<style lang="">
    
</style>