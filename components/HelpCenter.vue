<template lang="">
    <div class="max-w-full bg-[#F4F4F4]">
      <div class="absolute bg-[#D882D9] z-[2] bg-opacity-60 blur-[80px] rounded-full size-60 top-0 left-0"></div>
      <div class="absolute bg-[#D882D9]  bg-opacity-60 blur-[80px] rounded-md w-60 h-[80vh] top-0 right-0"></div>
<section class="overflow-hidden mx-6 max-w-7xlBig mx-auto relative z-[4] mt-6 rounded-3xl">
    <div class="relative w-full  mx-auto rounded-3xl  md:h-[550px] g-full bg-cover overflow-hidden  bg-start bg-no-repeat "
        style="background-image: url('https://img.freepik.com/free-vector/businessman-surrounded-by-opponents_23-2147620849.jpg?t=st=1733087467~exp=1733091067~hmac=29867c7686fd27c00206f89772746c31b49cd02f7ef42900c947f6296cbad79c&w=740');">

        <div class="absolute inset-0 rounded-3xl bg-gradient-to-r from-[#12013D] to-transparent"></div>


        <div class="relative flex  flex-col items-start justify-center h-full md:py-10 py-20">
            <div class="w-[80%]  mx-auto text-center text-white">
               <p class="my-4 md:text-[36px] text-2xl">The FAQS
                </p>
                <h1 class="text-[2.7rem] md:text-[4rem] font-bold leading-[70px] uppercase">Help Center</h1>
                <p class="mt-4 mx-auto md:text-[26px] font-extralight max-w-md text-lg">Everything you need to know about the product and building
                </p>
            </div>
        </div>
    </div>
    </section>


    <section class="bg-[#F4F4F4] py-6">
  <div class="max-w-7xlBig mx-auto mx-6 py-6 px-4">
    <h2 class="text-lg md:text-[26px] uppercase text-[#A988F5] mb-2">Introduction</h2>
    <p class="text-[#212121] text-[22px] font-extralight leading-relaxed">
      Lorem ipsum dolor sit amet, consectetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren.
    </p>
  </div>
</section>




<div class="bg-[#FAFAFA]">
  <!-- FAQ Section -->
  <section class=" grid md:grid-cols-2 max-w-7xlBig mx-auto grid-cols-1  gap-6 px-5 py-12">
    <div class="md:mt-5">
    <h2 class="text-3xl xl:text-[36px] text-[#3A0CA3] font-semibold uppercase text-[#3A0CA3] mb-4">Frequently Asked Questions</h2>
    <p class="text-[#212121]   mb-8 mt-5">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
    </p>
    </div>

    <!-- FAQ Items -->
    <div class="space-y-6">
      <div v-for="faq in faqs" :key="faq.id" class="border-b border-gray-200">
        <button 
          @click="toggleFaq(faq.id)"
          class="w-full flex justify-between items-center py-4 text-left focus:outline-none"
        >
          <span class="text-gray-800 text-lg font-medium">{{ faq.question }}</span>
          <span class="text-black border w-5 h-5 text-center flex justify-center items-center border-gray-700 rounded-full text-lg">
            <svg v-if="!faq.isOpen" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
              <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 5v14m-7-7h14"/>
            </svg>
            <svg v-else xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
              <path fill="currentColor" d="M18 12.998H6a1 1 0 0 1 0-2h12a1 1 0 0 1 0 2"/>
            </svg>
          </span>
        </button>
        <transition
          enter-active-class="transition duration-200 ease-out"
          leave-active-class="transition duration-200 ease-in"
          enter-from-class="transform scale-y-0 opacity-0"
          enter-to-class="transform scale-y-100 opacity-100"
          leave-from-class="transform scale-y-100 opacity-100"
          leave-to-class="transform scale-y-0 opacity-0"
        >
          <p v-show="faq.isOpen" class="text-gray-600 text-sm mt-2 pb-4">
            {{ faq.answer }}
          </p>
        </transition>
      </div>
    </div>
  </section>


</div>

  <!-- Contact Section -->
  <section class="bg-white rounded-b-3xl py-8">
    <div class="  justify-cente max-w-7xlBig mx-auto px-6 xl:px-0 mx-auto md:justify-between flex md:flex-row flex-col items-center text-center md:text-start">
      <div class="md:flex-row justify-center md:items-center items-center flex flex-col gap-4">

<div class="flex items-center size-[118px] bg-white shadow-xl flex items-center justify-center rounded-full gap-2">K</div>
      <div class="">
      <p class="text-gray-700 font-medium text-purple-700 text-lg mb-2">Still have questions?</p>
      <p class="text-gray-600 ">
        Can't find the answer you're looking for? Please chat with our friendly team.
      </p>
      </div>
    </div>

      <button class="px-6 py-2 bg-black text-white font-medium rounded-full  hover:bg-purple-800 transition">
        Get In Touch
      </button>
    </div>
  </section>

  </div>
</template>
<script>
export default {
  data() {
    return {
      faqs: [
        {
          id: 1,
          question: "Is there a free trial available?",
          answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonumy eirmod tempor invidunt ut labore et dolore.",
          isOpen: false
        },
        {
          id: 2,
          question: "Can I change my plan later?",
          answer: "Yes, you can change your plan at any time. Changes will be reflected in your next billing cycle.",
          isOpen: false
        },
        {
          id: 3,
          question: "What's your cancellation policy?",
          answer: "You can cancel your subscription at any time. No long-term contracts required.",
          isOpen: false
        },
        {
          id: 4,
          question: "Can other info be added to an invoice?",
          answer: "Yes, you can add custom information to your invoices through your account settings.",
          isOpen: false
        },
        {
          id: 5,
          question: "How does billing work?",
          answer: "We bill monthly on the date you signed up. You can view all billing details in your account.",
          isOpen: false
        },
        {
          id: 6,
          question: "How do I change my account email?",
          answer: "You can change your email address in your account settings section.",
          isOpen: false
        }
      ]
    }
  },
  methods: {
    toggleFaq(faqId) {
      this.faqs = this.faqs.map(faq => ({
        ...faq,
        isOpen: faq.id === faqId ? !faq.isOpen : false
      }))
    }
  }
}
</script>
<style lang="">
    
</style>