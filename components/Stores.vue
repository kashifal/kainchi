<template lang="">
   
      <main class="flex-1 bg-gray-100 md:p-8">
            <div class="md:p-5 md:px-10 p-2 mt-8 bg-white rounded-md shadow">
                <!-- Flex Layout for Form and Manage Everything Section -->
                <div class="flex flex-col gap-3 md:gap-20 md:flex-row">
                    <!-- Form Section -->
                    <div class="flex-1">
                        <form>
                            <h2 class="text-lg font-semibold text-gray-700">Let's know about your store</h2>
                            <p class="text-[12px] text-[#787878]">Lorem ipsum dolor sit amet consectetur adipisicing
                                elit. Architecto consequatur </p>

                            <div class="space-y-4 mt-[20px]">
                                <div>
                                    <label
                                        class="block  font-semibold text-[#656565] text-[14px] tracking-wider">What's
                                        your store name?</label>
                                    <input type="text"
                                        class="w-full px-4 py-4 bg-gray-100 border rounded-md focus:outline-none focus:ring focus:ring-indigo-300 mt-[6px]">
                                    <p class="text-[12px] text-[#787878] mt-[10px]">Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam dicta
                                        reiciendis, consequatur qui nihil provident, quasi exercitationem, libero odio
                                        nostrum sint pariatur consectetur.</p>
                                </div>
                                <div>
                                    <label
                                        class="block  font-semibold text-[#656565] text-[14px] tracking-wider">Are
                                        you building this store in your country?</label>
                                    <select
                                        class="w-full px-2 py-4 bg-gray-100 border rounded-md focus:outline-none focus:ring focus:ring-indigo-300 mt-[6px] text-[#BEBEBE]">
                                        <option>Choose a Country</option>
                                    </select>
                                </div>
                                <div>
                                    <label
                                        class="block  font-semibold text-[#656565] text-[14px] tracking-wider">What's
                                        your Currency?</label>
                                    <select
                                        class="w-full px-4 py-4 bg-gray-100 border rounded-md focus:outline-none focus:ring focus:ring-indigo-300  mt-[6px] text-[#BEBEBE]">
                                        <option>Choose a Currency</option>
                                    </select>
                                </div>
                            </div>
                            <button type="submit "
                                class="mt-6 bg-indigo-700 text-white px-6 py-3  rounded-full hover:bg-indigo-500 w-[100%]">Next</button>
                        </form>
                    </div>

                    <!-- Manage Everything Section -->
                    <div class="flex-1">
                        <div class="w-[100%] flex justify-center mt-10 md:mt-[170px]">
                            <img src="https://scontent.xx.fbcdn.net/v/t1.15752-9/462561827_1639717936941294_3044994882706943328_n.jpg?stp=dst-jpg_s480x480&_nc_cat=111&ccb=1-7&_nc_sid=0024fc&_nc_ohc=c6X0lqM1HzEQ7kNvgG6IG0F&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent.xx&oh=03_Q7cD1QHxuicJhGkNJe0YyTNEcZqZYrMKt79fp4CvK7IXyTnmFQ&oe=677289DC" class="h-[40px]" alt="">
                        </div>
                        <div class="md:mt-[130px] mt-5 md:ml-0  w-full p-3  rounded-2xl border-2 ">
                            <p class="font-semibold mb-3 text-[1.4rem]">Manage - everything</p>
                            <p class="text-[11px] text-gray-600">Lorem ipsum dolor sit amet, consectetur<br> amet consectetur adipisicing elit. Veniam non velit obcaecati <br> dolor incidunt praesentium dolor! Recusandae impedi </p>
                            
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