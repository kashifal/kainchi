<template lang="">

    <div class="my-20 py-20 overflow-hidden border-t border-b border-[#707070] bg-[#212121] text-white relative">
        <!-- Left bottom decorative SVGs -->
        <div class="absolute left-8 bottom-8 flex gap-4 opacity-10">
           
            <svg xmlns="http://www.w3.org/2000/svg"  class="size-12 rotate-45 md:size-16 lg:size-28" width="16" height="16" viewBox="0 0 16 16"><path fill="currentColor" d="M9 11H6c0-3 1.6-4 2.7-4.6q.6-.3.9-.6c.5-.5.3-1.2.2-1.4c-.3-.7-1-1.4-2.3-1.4C5.4 3 5 4.9 5 5.3l-3-.4C2.2 3.2 3.7 0 7.5 0c2.3 0 4.3 1.3 5.1 3.2c.7 1.7.4 3.5-.8 4.7c-.5.5-1.1.8-1.6 1.1c-.9.5-1.2 1-1.2 2m.5 3a2 2 0 1 1-3.999.001A2 2 0 0 1 9.5 14"/></svg>
            <svg xmlns="http://www.w3.org/2000/svg"  class="size-12 rotate-45 md:size-16 lg:size-16" width="16" height="16" viewBox="0 0 16 16"><path fill="currentColor" d="M9 11H6c0-3 1.6-4 2.7-4.6q.6-.3.9-.6c.5-.5.3-1.2.2-1.4c-.3-.7-1-1.4-2.3-1.4C5.4 3 5 4.9 5 5.3l-3-.4C2.2 3.2 3.7 0 7.5 0c2.3 0 4.3 1.3 5.1 3.2c.7 1.7.4 3.5-.8 4.7c-.5.5-1.1.8-1.6 1.1c-.9.5-1.2 1-1.2 2m.5 3a2 2 0 1 1-3.999.001A2 2 0 0 1 9.5 14"/></svg>

        </div>

        <!-- Right bottom decorative SVGs -->
        <div class="absolute right-10 bottom-10 flex gap-4 opacity-10">
          <svg xmlns="http://www.w3.org/2000/svg"  class="size-12 -rotate-45 md:size-16 lg:size-28" width="16" height="16" viewBox="0 0 16 16"><path fill="currentColor" d="M9 11H6c0-3 1.6-4 2.7-4.6q.6-.3.9-.6c.5-.5.3-1.2.2-1.4c-.3-.7-1-1.4-2.3-1.4C5.4 3 5 4.9 5 5.3l-3-.4C2.2 3.2 3.7 0 7.5 0c2.3 0 4.3 1.3 5.1 3.2c.7 1.7.4 3.5-.8 4.7c-.5.5-1.1.8-1.6 1.1c-.9.5-1.2 1-1.2 2m.5 3a2 2 0 1 1-3.999.001A2 2 0 0 1 9.5 14"/></svg>

        </div>

        <div class="container mx-auto px-4">
            <h1 class="md:text-[36px] text-center sm:text-[30px] text-[25px] font-bold">Frequently Asked Questions</h1>
            <p class="sm:text-[18px] text-[16px] py-1 text-center max-w-2xl mx-auto">
                Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore.
            </p>
        </div>

        <div class="flex items-center my-20">
            <div class="relative w-full overflow-hidden">
                <div class="flex px-4">
                    <div class="flex gap-8 transition-transform duration-500 w-[120%] -ml-[10%]" 
                         :style="slideStyle">
                        <div v-for="(card, index) in cards" :key="index" 
                             class="w-[150vw] md:w-[100vw] md:h-[50vh] h-full transition-all duration-500"
                             :class="{ 
                                'scale-100 translate-x-0 opacity-100 w-[200%] sm:w-[150vw]': currentSlide === index,
                                'sm:scale-95 opacity-70 -translate-x-1/4': currentSlide > index,
                                'sm:scale-95 opacity-70 translate-x-1/4': currentSlide < index
                             }">
                            <div class="bg-[#292929] flex items-start justify-center flex-col shadow-[0px_3px_10px_#00000080] h-full p-5 md:p-6 lg:p-10 rounded-[20px]">
                                <h1 class="text-[#FFF7C4] text-[18px] sm:text-[20px] md:text-[24px] lg:text-[28px] font-semibold">{{ card.title }}</h1>
                                <p class="text-[14px] md:text-[16px] my-3 md:my-4">{{ card.description1 }}</p>
                                <p class="text-[14px] md:text-[16px]">{{ card.description2 }}</p>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="flex mb-2 justify-center gap-2 mt-10">
                    <button v-for="(_, index) in cards" 
                            :key="index"
                            @click="goToSlide(index)"
                            class="w-2 h-2 md:w-3 md:h-3 rounded-full transition-all duration-300"
                            :class="currentSlide === index ? 'bg-white scale-125' : 'bg-white/30 scale-100'">
                    </button>
                </div>
            </div>
        </div>

        <div class="text-center px-4">
            <p class="text-[16px] md:text-[18px] mb-4">You still have questions?</p>
            <button class="px-5 md:px-7 py-2 md:py-2.5 group text-[16px] md:text-[18px] hover:gap-8 transition-all duration-200 bg-white rounded-full mx-auto font-medium text-[#480CA8] flex items-center gap-3 inline-flex">
                See More
                <svg xmlns="http://www.w3.org/2000/svg" class="size-5 md:size-6" width="1em" height="1em" viewBox="0 0 24 24">
                    <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 17L17 7M7 7h10v10"/>
                </svg>
            </button>
        </div>
    </div>
</template>
<script>
export default {
  data() {
    return {
      currentSlide: 1,
      autoSlideInterval: null,
      cards: [
      {
          title: "Is Kain'chi right for my business ?",
          description1: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore.",
          description2: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore."
        },
        {
          title: "Is Kain'chi right for my business ?",
          description1: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore.",
          description2: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore."
        },
        {
          title: "Is Kain'chi right for my business ?",
          description1: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore.",
          description2: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore."
        },
      ]
    }
  },
  methods: {
    goToSlide(index) {
      this.currentSlide = index;
    },
    nextSlide() {
      this.currentSlide = (this.currentSlide + 1) % this.cards.length;
    },
    getTransformValue() {
      const slideWidth = 33.33;
      return `translateX(${-slideWidth * this.currentSlide + 33.33}%)`;
    }
  },
  computed: {
    slideStyle() {
      return {
        transform: this.getTransformValue()
      }
    }
  }
}
</script>
<style lang="">

</style>