<template>
    <section class="bg-[#F5F1FE] py-20">
        <div class="max-w-7xlBig px-4 mx-auto grid gap-[3rem] grid-cols-1 md:grid-cols-2">
            <div class="md:ml-28 md:max-w-[60%] lg:max-w-[50%]">
                <div class="text-[#3E2CA3]">
                    <h1 class="text-[3rem] font-extrabold leading-[55px]">ABOUT <br> KAAINCHI</h1>
                </div>
                <div class="mt-[60px]">
                    <h2 class="text-[1.7rem] font-semibold text-gray-800">We are on a mission!</h2>
                    <p class="text-[12px] mt-[15px] text-[#6B6B6B]">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Pariatur facilis mollitia quam dolore dolor ducimus optio, nemo odio repellat maxime voluptas tenetur nemo odio repellat maxime voluptas tenetur..</p>
                    <p class="text-[12px] mt-[15px] text-[#6B6B6B]">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Pariatur facilis mollitia quam dolore dolor ducimus optio, nemo odio repellat maxime voluptas tenetur. nemo odio repellat maxime voluptas tenetur.</p>
                    <p class="text-[12px] mt-[15px] text-[#6B6B6B]">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Pariatur facilis mollitia quam dolore dolor ducimus optio, nemo odio repellat maxime voluptas tenetur. nemo odio repellat maxime voluptas tenetur.</p>
                </div>
            </div>
            <div class="relative">
                <img 
                    :src="images[currentSlide]" 
                    class="h-[500px] rounded-3xl w-full md:w-[75%] object-cover" 
                    alt="Carousel Image"
                >
                <div class="flex flex-wrap items-center justify-between mt-4">
                    <div class="flex justify-between w-full md:w-[75%] gap-2">
                        <div class="flex gap-4">
                            <button @click="prevSlide" class="flex h-[40px] w-[40px] cursor-pointer items-center justify-center rounded-full border border-gray-500 text-gray-500 hover:bg-black hover:text-white transition-all duration-300">
                                <svg xmlns="http://www.w3.org/2000/svg" width="1.2em" height="1.2em" viewBox="0 0 24 24"><path fill="currentColor" d="M12.727 3.687a1 1 0 1 0-1.454-1.374l-8.5 9a1 1 0 0 0 0 1.374l8.5 9.001a1 1 0 1 0 1.454-1.373L4.875 12z" /></svg>
                            </button>
                            <button @click="nextSlide" class="flex h-[40px] w-[40px] rotate-180 cursor-pointer items-center justify-center rounded-full border border-gray-500 text-gray-500 hover:bg-black hover:text-white transition-all duration-300">
                                <svg xmlns="http://www.w3.org/2000/svg" width="1.2em" height="1.2em" viewBox="0 0 24 24"><path fill="currentColor" d="M12.727 3.687a1 1 0 1 0-1.454-1.374l-8.5 9a1 1 0 0 0 0 1.374l8.5 9.001a1 1 0 1 0 1.454-1.373L4.875 12z" /></svg>
                            </button>
                        </div>
                        <div class="flex items-center gap-2">
                            <button 
                                v-for="(_, index) in images" 
                                :key="index" 
                                @click="goToSlide(index)"
                                class="h-3 rounded-full cursor-pointer transition-all duration-300"
                                :class="[
                                    currentSlide === index 
                                        ? 'bg-[#3A0CA3] w-[41px]' 
                                        : 'bg-[#C2C2C2] w-[13px] hover:bg-[#3A0CA3]/50'
                                ]"
                            ></button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            currentSlide: 0,
            images: [
                'https://img.freepik.com/premium-photo/muslim-woman-model-wearing-hijab-show-muslim-religious-photography_1020867-59366.jpg',
                'https://i.ytimg.com/vi/6zZoj9JCA44/hqdefault.jpg',
                'https://i.pinimg.com/474x/2a/6b/60/2a6b60413815eff061a6d10a7ac6295e.jpg',
                'https://i.pinimg.com/474x/4d/84/80/4d848035ad93b63bb42d3fff721c95e4.jpg',
            ]
        }
    },
    methods: {
        nextSlide() {
            this.currentSlide = (this.currentSlide + 1) % this.images.length
        },
        prevSlide() {
            this.currentSlide = (this.currentSlide - 1 + this.images.length) % this.images.length
        },
        goToSlide(index) {
            this.currentSlide = index
        }
    }
}
</script>
<style lang="">

</style>