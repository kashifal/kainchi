<template lang="">
      <main class="flex-1 p-8">
            <header class="flex items-center">
                <h1 class="text-2xl font-semibold text-gray-700">Stores</h1>

                <!-- Number Line Section -->
                <div class="flex items-center justify-around w-full ">
                    <div
                        class="flex items-center justify-center w-10 h-10 font-bold text-white bg-indigo-500 rounded-full">
                        1</div>
                    <div class="w-40 h-2 bg-white"></div>
                    <div class="flex items-center justify-center w-10 h-10 font-bold text-black bg-white rounded-full">2
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
                <!-- Flex Layout for Form and Manage Everything Section -->
                <div class="flex space-x-8">
                    <!-- Form Section -->
                    <div class="flex-1">
                        <form>
                            <h2 class="text-lg font-bold text-gray-700">Let's know about your store</h2>
                            <p class="text-[12px] text-[#787878]">Lorem ipsum dolor sit amet consectetur adipisicing
                                elit. Architecto consequatur </p>

                            <div class="space-y-4 mt-[20px]">
                                <div>
                                    <label
                                        class="block text-gray-700 font-bold text-[#656565] text-[14px] tracking-wider">What's
                                        your store name?</label>
                                    <input type="text"
                                        class="w-full px-4 py-4 bg-gray-100 border rounded-md focus:outline-none focus:ring focus:ring-indigo-300 mt-[6px]">
                                    <p class="text-[12px] text-[#787878] mt-[10px]">Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam dicta
                                        reiciendis, consequatur qui nihil provident, quasi exercitationem, libero odio
                                        nostrum sint pariatur consectetur.</p>
                                </div>
                                <div>
                                    <label
                                        class="block text-gray-700 font-bold text-[#656565] text-[14px] tracking-wider">Are
                                        you building this store in your country?</label>
                                    <select
                                        class="w-full px-2 py-4 bg-gray-100 border rounded-md focus:outline-none focus:ring focus:ring-indigo-300 mt-[6px] text-[#BEBEBE]">
                                        <option>Choose a Country</option>
                                    </select>
                                </div>
                                <div>
                                    <label
                                        class="block text-gray-700 font-bold text-[#656565] text-[14px] tracking-wider">What's
                                        your Currency?</label>
                                    <select
                                        class="w-full px-4 py-4 bg-gray-100 border rounded-md focus:outline-none focus:ring focus:ring-indigo-300  mt-[6px] text-[#BEBEBE]">
                                        <option>Choose a Currency</option>
                                    </select>
                                </div>
                            </div>
                            <button type="submit "
                                class="mt-6 bg-indigo-600 text-white px-6 py-2 rounded-full hover:bg-indigo-500 w-[100%]">Next</button>
                        </form>
                    </div>

                    <!-- Manage Everything Section -->
                    <div class="flex-1">
                        <div class="w-[100%] flex justify-center mt-[170px]">
                            <!-- <img src="./ci--image-02.svg" class="h-[40px]" alt=""> -->

                        </div>
                        <div class="mt-[100px] p-4  rounded-lg border-2 ">
                            <p class="font-bold text-[1.4rem]">Manage - everything</p>
                            <p class="text-[12px] text-gray-600">Lorem ipsum dolor sit amet, consectetur<br> amet consectetur adipisicing elit. Veniam non velit obcaecati <br> dolor incidunt praesentium dolor! Recusandae impedi </p>
                            
                        </div>
                    </div>
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