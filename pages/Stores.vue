<template lang="">
    <div>
    <div class="mx-auto bg-gray-100">
      <header class="flex w-full pt-10 max-w-7xl mx-auto xl:flex-row flex-col items-center">
                <h1 class="text-2xl mr-7 font-semibold text-gray-700">Stores</h1>

                <!-- Number Line Se
                 ction -->
                <div class="flex mx-auto max-w-7xl">
                    <div class="flex items-center justify-around w-fit ">
                        <div
                            @click="activeStore = 1"
                            :class="{
                                'bg-indigo-500 text-white': activeStore >= 1,
                                'bg-white text-black': activeStore < 1
                            }"
                            class="flex items-center justify-center w-10 h-10 font-bold rounded-full cursor-pointer">
                            1</div>
                        <div 
                            class="h-1 w-[14vw]"
                            :class="{'bg-indigo-500': activeStore >= 2, 'bg-white': activeStore < 2}">
                        </div>
                        <div
                            @click="activeStore = 2"
                            :class="{
                                'bg-indigo-500 text-white': activeStore >= 2,
                                'bg-white text-black': activeStore < 2
                            }"
                            class="flex items-center justify-center w-10 h-10 font-bold rounded-full cursor-pointer">
                            2</div>
                        <div 
                            class="h-1 w-[14vw]"
                            :class="{'bg-indigo-500': activeStore >= 3, 'bg-white': activeStore < 3}">
                        </div>
                        <div
                            @click="activeStore = 3"
                            :class="{
                                'bg-indigo-500 text-white': activeStore >= 3,
                                'bg-white text-black': activeStore < 3
                            }"
                            class="flex items-center justify-center w-10 h-10 font-bold rounded-full cursor-pointer">
                            3</div>
                        <div 
                            class="h-1 w-[14vw]"
                            :class="{'bg-indigo-500': activeStore >= 4, 'bg-white': activeStore < 4}">
                        </div>
                        <div
                            @click="activeStore = 4"
                            :class="{
                                'bg-indigo-500 text-white': activeStore >= 4,
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