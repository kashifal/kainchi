<template lang="">
    <div class="bg-white mb-40 py-40 lg:py-20 rounded-b-[60px] md:rounded-b-[100px] shadow-[0_100px_99px_#00000008]">
      <div class="max-w-7xl min-h-[500px] h-full mx-auto px-4 grid lg:grid-cols-2 gap-10 lg:gap-2">
        <div class="h-full flex flex-col items-start justify-between gap-3">
          <div>
            <h1
              class="lg:text-[56px] md:text-[40px] text-[30px] leading-none text-[#3A0CA3] font-semibold"
              v-html="formattedTitle"
            ></h1>
            <p class="text-[#212121] py-4 md:text-[22px] sm:text-[18px]">
              Learn more about what you can do on Kainchi.
            </p>
          </div>
          <div class="flex items-center gap-3">
            <div
              class="border-[#BEBEBE] hover:bg-[#BEBEBE] cursor-pointer rotate-180 rounded-full border size-[54px] flex items-center justify-center"
            >
              <svg
                class="size-5"
                xmlns="http://www.w3.org/2000/svg"
                width="1em"
                height="1em"
                viewBox="0 0 24 24"
              >
                <path
                  fill="none"
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="m10 17l5-5l-5-5"
                />
              </svg>
            </div>
            <div
              class="border-[#BEBEBE] hover:bg-[#BEBEBE] cursor-pointer rounded-full border size-[54px] flex items-center justify-center"
            >
              <svg
                class="size-5"
                xmlns="http://www.w3.org/2000/svg"
                width="1em"
                height="1em"
                viewBox="0 0 24 24"
              >
                <path
                  fill="none"
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="m10 17l5-5l-5-5"
                />
              </svg>
            </div>
          </div>
        </div>
  
        <div class="lg:flex grid sm:grid-cols-2 md:grid-cols-3 gap-y-10 gap-x-2 text-[#212121]">
          <div
            v-for="(card, index) in cards"
            :key="index"
            class="h-full lg:w-1/3 text-wrap cursor-pointer group "
          >
            <div class="group shadow-[0_3px_10px_#00000029] relative rounded-[25px] w-full 2xl:rounded-[30px] overflow-hidden">
              <img
                class=" group-hover:scale-[0.98] transition-all duration-400 h-[200px] 2xl:h-[300px] object-cover  w-full"
                :src="card.image"
                :alt="card.title"
              />
              <div class="group-hover:bg-black/50 transition-all duration-400 h-full w-full absolute top-0 left-0"></div>
            </div>
            <h1
              class="2xl:text-[36px]  text-wrap text-[30px] font-medium leading-none py-4"
            >
              {{ card.title }}
            </h1>
            <div class="flex items-center gap-2">
              <a
                :href="card.link"
                class="sm:text-[18px] py-1 border-b border-[#3A0CA3]"
              >
                Learn more
              </a>
              <svg
                class="size-5"
                xmlns="http://www.w3.org/2000/svg"
                width="1em"
                height="1em"
                viewBox="0 0 24 24"
              >
                <path
                  fill="none"
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="m10 17l5-5l-5-5"
                />
              </svg>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        title: "ALREADY DOWNLOADED?<br>Do More with Us",
        cards: [
          {
            title: "Build Community",
            image:
              "https://images.unsplash.com/photo-1732444827571-3b16b9a837e4?q=80&w=1414&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
            link: "#",
          },
          {
            title: "Build Community",
            image:
              "https://images.unsplash.com/photo-1580687581604-0e57ffe41812?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
            link: "#",
          },
          {
            title: "Message Privately",
            image:
              "https://plus.unsplash.com/premium_photo-1666985732128-b8acafd17652?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
            link: "#",
          },
        ],
      };
    },
    computed: {
      formattedTitle() {
        return this.title;
      },
    },
  };
  </script>
  
  <style lang=""></style>
  