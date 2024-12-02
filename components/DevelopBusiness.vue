<template>
    <div class="max-w-7xl mx-auto px-4 py-32">
      <div class="grid md:grid-cols-2 gap-12">
        <img
          src="/blockMAn.jpeg"
          alt="Main Image"
          class="w-full object-cover"
        />
        <div>
          <h1 class="lg:text-[50px] text-4xl text-[#212121] leading-tight font-semibold">
            Create and develop your business with
            <p class="text-[#3A0CA3] inline">Kain'chi</p>
          </h1>
          <p class="text-[#212121] pt-3 pb-5">
            Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
          </p>
  
          <div class="mt-6 grid grid-cols-1 gap-6">
            <div
              v-for="(card, index) in cards"
              :key="index"
              class="flex items-start gap-5"
            >

              <div
                class="md:size-[94px] shrink-0 text-[30px] size-[70px] text-white bg-[#5E19CF] rounded-[10px] flex items-center justify-center"
                v-html="card.svg"
              ></div>

              <div>
                <h1 class="text-[#5E19CF] text-[22px] font-semibold">
                  {{ card.title }}
                </h1>
                <p class="text-[#656565] md:text-[18px] pt-[2px]">{{ card.description }}</p>
              </div>
            </div>
          </div>

          <button class="bg-[#212121] mt-10 hover:bg-opacity-90 rounded-full w-full px-4 text-center text-white text-[18px] md:text-[19px] py-2.5 md:py-[18px]">Let's Start Building Your Store !</button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        cards: [
          {
            title: "Customize your store",
            description:
              "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore.",
            svg: `
              <svg  class="md:size-[30px] size-[22px]" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 20h1m-4 0h-2v-3m3 0h3v-3h-1m-5 0h2M4 17c0-.932 0-1.398.152-1.766a2 2 0 0 1 1.082-1.082C5.602 14 6.068 14 7 14s1.398 0 1.766.152c.49.203.879.592 1.082 1.082c.152.368.152.834.152 1.766s0 1.398-.152 1.765a2 2 0 0 1-1.082 1.083C8.398 20 7.932 20 7 20s-1.398 0-1.766-.152a2 2 0 0 1-1.082-1.082C4 18.398 4 17.932 4 17M14 7c0-.932 0-1.398.152-1.766a2 2 0 0 1 1.082-1.082C15.602 4 16.068 4 17 4s1.398 0 1.766.152c.49.203.879.592 1.082 1.082C20 5.602 20 6.068 20 7s0 1.398-.152 1.765a2 2 0 0 1-1.082 1.083C18.398 10 17.932 10 17 10s-1.398 0-1.766-.152a2 2 0 0 1-1.082-1.082C14 8.398 14 7.932 14 7M4 7c0-.932 0-1.398.152-1.766a2 2 0 0 1 1.082-1.082C5.602 4 6.068 4 7 4s1.398 0 1.766.152c.49.203.879.592 1.082 1.082C10 5.602 10 6.068 10 7s0 1.398-.152 1.765a2 2 0 0 1-1.082 1.083C8.398 10 7.932 10 7 10s-1.398 0-1.766-.152a2 2 0 0 1-1.082-1.082C4 8.398 4 7.932 4 7"/></svg>
            `,
          },
          {
            title: "Drive your business",
            description:
            "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore.",
            svg: `
              <svg  class="md:size-[30px] size-[22px]" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="M20 12a2 2 0 0 0-.703.133l-2.398-1.963c.059-.214.101-.436.101-.67C17 8.114 15.886 7 14.5 7S12 8.114 12 9.5c0 .396.1.765.262 1.097l-2.909 3.438A2 2 0 0 0 9 14c-.179 0-.348.03-.512.074l-2.563-2.563C5.97 11.348 6 11.179 6 11c0-1.108-.892-2-2-2s-2 .892-2 2s.892 2 2 2c.179 0 .348-.03.512-.074l2.563 2.563A2 2 0 0 0 7 16c0 1.108.892 2 2 2s2-.892 2-2c0-.237-.048-.46-.123-.671l2.913-3.442c.227.066.462.113.71.113a2.5 2.5 0 0 0 1.133-.281l2.399 1.963A2 2 0 0 0 18 14c0 1.108.892 2 2 2s2-.892 2-2s-.892-2-2-2"/></svg>
            `,
          },
          {
            title: "Sell globally",
            description:
            "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore.",
            svg: `
             <svg class="md:size-[30px] size-[22px]" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 48 48"><defs><mask id="ipTTrace0"><g fill="none" stroke="#fff" stroke-linejoin="round" stroke-width="4"><path stroke-linecap="round" d="M24 6C14.059 6 6 14.059 6 24s8.059 18 18 18s18-8.059 18-18"/><path stroke-linecap="round" d="M24 15a9 9 0 1 0 9 9m-9 0l6.3-6.306"/><path fill="#555" d="M30.3 11.426V17.7h6.325L42 12.3h-6.297V6z"/></g></mask></defs><path fill="currentColor" d="M0 0h48v48H0z" mask="url(#ipTTrace0)"/></svg>
            `,
          },
          {
            title: "Attreact visitors",
            description:
            "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore.",
            svg: `
              <svg class="md:size-[30px] size-[22px]" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><g class="scope-outline"><g fill="currentColor" fill-rule="evenodd" class="Vector" clip-rule="evenodd"><path d="M19.598 9.495a8 8 0 1 1-15.194 5.01a8 8 0 0 1 15.194-5.01m-1.614 2.95a6.001 6.001 0 1 0-11.97-.89a6.001 6.001 0 0 0 11.97.89"/><path d="M12 14a2 2 0 1 0 0-4a2 2 0 0 0 0 4m0 2a4 4 0 1 0 0-8a4 4 0 0 0 0 8m0-14a1 1 0 0 1 1 1v2a1 1 0 1 1-2 0V3a1 1 0 0 1 1-1m0 16a1 1 0 0 1 1 1v2a1 1 0 1 1-2 0v-2a1 1 0 0 1 1-1m10-6a1 1 0 0 1-1 1h-2a1 1 0 1 1 0-2h2a1 1 0 0 1 1 1M6 12a1 1 0 0 1-1 1H3a1 1 0 1 1 0-2h2a1 1 0 0 1 1 1"/></g></g></svg>
            `,
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  /* Additional styles if needed */
  </style>
  