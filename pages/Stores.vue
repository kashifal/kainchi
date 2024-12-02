<template lang="">
    <div class="flex-1  min-h-screen h-full px-2 xl:px-8 pt-28 pb-20 rounded-lg  bg-[#E3E3E5]">
        <div class="py-4">
      <nav class="text-sm text-gray-600">
        <span class="hover:underline cursor-pointer">Dashboard</span>
        <span class="mx-2">></span>
        <span class="hover:underline cursor-pointer">Stores</span>
        <span class="mx-2">></span>
        <span class="font-semibold text-gray-800">New</span>
      </nav>
    </div>
    <div class="mx-auto">
      <header class="flex w-full pt-10  text-[#212121]  xl:flex-row flex-col items-center">
                <h1 class="text-2xl xl:text-[36px] mr-7 mb-5 xl:mb-0 font-semibold">Stores</h1>

                <!-- Number Line Se
                 ction -->
                <div class="flex mx-auto   ">
                    <div class="flex items-center justify-around w-fit ">
                        <div
                            @click="activeStore = 1"
                            :class="{
                                'bg-[#3A0CA3] text-white': activeStore >= 1,
                                'bg-white text-black': activeStore < 1
                            }"
                            class="flex items-center justify-center w-10 h-10 font-bold rounded-full cursor-pointer">
                            1</div>
                        <div 
                            class="h-1 w-[14vw]"
                            :class="{'bg-[#3A0CA3]': activeStore >= 2, 'bg-white': activeStore < 2}">
                        </div>
                        <div
                            @click="activeStore = 2"
                            :class="{
                                'bg-[#3A0CA3] text-white': activeStore >= 2,
                                'bg-white text-black': activeStore < 2
                            }"
                            class="flex items-center justify-center w-10 h-10 font-bold rounded-full cursor-pointer">
                            2</div>
                        <div 
                            class="h-1 w-[14vw]"
                            :class="{'bg-[#3A0CA3]': activeStore >= 3, 'bg-white': activeStore < 3}">
                        </div>
                        <div
                            @click="activeStore = 3"
                            :class="{
                                'bg-[#3A0CA3] text-white': activeStore >= 3,
                                'bg-white text-black': activeStore < 3
                            }"
                            class="flex items-center justify-center w-10 h-10 font-bold rounded-full cursor-pointer">
                            3</div>
                        <div 
                            class="h-1 w-[14vw]"
                            :class="{'bg-[#3A0CA3]': activeStore >= 4, 'bg-white': activeStore < 4}">
                        </div>
                        <div
                            @click="activeStore = 4"
                            :class="{
                                'bg-[#3A0CA3] text-white': activeStore >= 4,
                                'bg-white text-black': activeStore < 4
                            }"
                            class="flex items-center justify-center w-10 h-10 font-bold rounded-full cursor-pointer">
                            4</div>
                    </div>
                </div>
            </header>
    </div>
        <Stores v-if="activeStore === 1" />
        <Stores2 v-if="activeStore === 2" />
        <Stores3 v-if="activeStore === 3" />
        <Stores4 v-if="activeStore === 4" />
    </div>
</template>
<script>
export default {
    data() {
        return {
            activeStore: 1
        }
    }
}
</script>
<style lang="">
    
</style>