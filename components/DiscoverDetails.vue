<template lang="html">
    <div class="bg-[#212121] my-20 rounded-[50px]    max-w-7xlBig mx-auto p-10">
      <h1 class="text-white text-center text-3xl lg:text-[36px] uppercase font-bold">DISCOVER OUR DEALS BY CATEGORY</h1>
      <div class="mt-28 2xl:max-w-6xl mx-auto gap-x-3 gap-y-14 grid sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
        <div
          v-for="(card, index) in cards"
          :key="index"
          class="bg-white group flex gap-5 flex-col items-center justify-center rounded-[30px] p-2 border border-[#480CA8] cursor-pointer"
        >
          <div class="w-full h-fit rounded-[30px] overflow-hidden">
            <img
              :src="card.image"
              :alt="card.title"
              class="h-[259px] group-hover:scale-125 rounded-[30px] object-cover transition-all duration-500 w-full"
            />
          </div>
          <button
            class="border mb-2 border-[#3A0CA3] group-hover:bg-[#3A0CA3] whitespace-nowrap group-hover:text-white text-[#3A0CA3] md:py-2 py-1.5 md:text-[18px] text-center font-medium lg:py-2.5 px-7 sm:px-8 lg:px-10 rounded-full"
          >
            {{ card.title }}
          </button>
        </div>
      </div>
      <button class="px-7 py-2.5 group md:text-[18px] hover:gap-8 transition-all duration-200 mt-20 bg-white rounded-full mx-auto font-medium text-[#480CA8] flex items-center gap-3">
        Next Page
        <svg xmlns="http://www.w3.org/2000/svg" class="size-6 " width="1em" height="1em" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 17L17 7M7 7h10v10"/></svg>
      </button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        // Define the data for each card here
        cards: [
          { title: 'Electronics', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' },
          { title: 'Jobs', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' },
          { title: 'Real State', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' },
          { title: 'Automotive', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' },
          { title: 'Furnishings', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' },
          { title: 'Pets', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' },
          { title: 'Clothes', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' },
          { title: 'Services', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' },
          { title: 'Professional Materials', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' },
          { title: 'Antiques', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' },
          { title: 'Gaming', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' },
          { title: 'Arts', image: 'https://images.unsplash.com/photo-1732496742791-8e3e7ba5c385?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' }
        ]
      }
    }
  }
  </script>
  
  <style>
  </style>
  