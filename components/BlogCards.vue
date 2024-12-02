<template lang="">
   <div class="px-4">
    <section class="  pt-[100px] pb-[100px]">

        <div class="max-w-7xl mx-auto">
        <h1 class="text-[3rem]">Topic match for you</h1>
        <div class="flex mt-[20px] gap-4 flex-wrap ">
            <button class="bg-[black] shadow-2xl text-[white] py-[10px] px-[50px] rounded-full">Design</button>
            <button class="bg-[white] hover:shadow-2xl  hover:bg-black hover:text-white text-[black] border-[1px] border-black py-[10px] px-[50px] rounded-full">Technology</button>
            <button class="bg-[white] hover:shadow-2xl  hover:bg-black hover:text-white text-[black] border-[1px] border-black py-[10px] px-[50px] rounded-full">Programming</button>
            <button class="bg-[white] hover:shadow-2xl  hover:bg-black hover:text-white text-[black] border-[1px] border-black py-[10px] px-[50px] rounded-full">Updates</button>
            <button class="bg-[white] hover:shadow-2xl  hover:bg-black hover:text-white text-[black] border-[1px] border-black py-[10px] px-[50px] rounded-full">Programming</button>
        </div>
    </div>


    </section>



    <section class="pb-[100px]">
   

   

        <div class="max-w-7xl mx-auto grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-x-2 gap-y-10 xl:gap-8 bg-[#EBEBEB]">
    <div
      v-for="(card, index) in cards"
      :key="index"
      class="bg-white rounded-2xl shadow-lg overflow-hidden"
    >
      <!-- Card Image -->
      <img
  class="h-48 w-full object-fill"
  :src="card.image"
/>


      <!-- Card Content -->
      <div class="p-6">
        <h2 class="text-[18px] font-bold text-[#3E2CA3] mb-2">
          {{ card.title }}
        </h2>
        <p class="text-gray-600 mb-6 text-[12px]">{{ card.description }}</p>

        <!-- User Info -->
        <div class="flex items-center mt-[20px]">
          <img
            class="w-10 h-10 rounded-full mr-4"
            :src="card.userImage"
            alt="User Image"
          />
          <div class="flex items-center space-x-2">
            <span class="text-gray-500">by</span>
            <span class="font-semibold text-gray-700 text-[14px]">
              {{ card.author }}
            </span>
          </div>
          <span class="ml-auto text-gray-500 text-[12px] mt-[4px]">
            {{ card.readTime }}
          </span>
        </div>
      </div>
    </div>
  </div>

  

    <!-- Pagination Buttons -->
    <div class="flex justify-center items-center space-x-4 mt-10">
      
    
        
        <div class="flex space-x-2 text-lg font-semibold text-gray-700">
            <div class="sm:size-[64px] size-[40px] border border-transparent hover:border-gray-700 rounded-full hover:bg-[#212121] hover:text-white flex items-center justify-center cursor-pointer ">
                           <svg xmlns="http://www.w3.org/2000/svg" width="1.5em" height="1.5em" viewBox="0 0 24 24"><path fill="currentColor" d="M12.727 3.687a1 1 0 1 0-1.454-1.374l-8.5 9a1 1 0 0 0 0 1.374l8.5 9.001a1 1 0 1 0 1.454-1.373L4.875 12z"/></svg>
                          </div>
            <span class="sm:size-[64px] size-[40px] rounded-full bg-[#212121] text-white flex items-center justify-center cursor-pointer border border-[#21212142] shadow-md">1</span>
            <span class="sm:size-[64px] size-[40px] rounded-full hover:bg-[#212121] hover:text-white flex items-center justify-center cursor-pointer border border-[#21212142] shadow-md">2</span>
            <span class="sm:size-[64px] size-[40px] rounded-full hover:bg-[#212121] hover:text-white flex items-center justify-center cursor-pointer border border-[#21212142] shadow-md">3</span>
            <span class="sm:size-[64px] size-[40px] rounded-full hover:bg-[#212121] hover:text-white flex items-center justify-center cursor-pointer border border-[#21212142] shadow-md">4</span>
                         
                          <div class="sm:size-[64px] size-[40px] border border-transparent hover:border-gray-700 rounded-full hover:bg-[#212121] hover:text-white rotate-180  flex items-center justify-center cursor-pointer ">
                           <svg xmlns="http://www.w3.org/2000/svg"  width="1.5em" height="1.5em" viewBox="0 0 24 24"><path fill="currentColor" d="M12.727 3.687a1 1 0 1 0-1.454-1.374l-8.5 9a1 1 0 0 0 0 1.374l8.5 9.001a1 1 0 1 0 1.454-1.373L4.875 12z"/></svg>
                          </div>
        </div>
    
        
      
    </div>
    

    
    </section>
    
    

</div>
</template>
<script>
export default {
    data() {
        return {
            cards: [
                {
                    image:
                        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRuj0oHm1mEbQ3hs6H9SMOZtKLYo9eowgYyuw&s",
                    title: "The Latest Update of Kainchi App",
                    description:
                        "The Privacy Policy is intended to clarify the manner in which your personal information.",
                    userImage:
                        "https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?w=100&h=100&fit=crop",
                    author: "Hamza Kainchi",
                    readTime: "5 min Read",
                },
                {
                    image:
                        "https://i1.sndcdn.com/artworks-4xyMjv43zWgNyCvt-XtF19Q-t500x500.jpg",
                    title: "Explore Vue.js 3 Features",
                    description:
                        "Learn about the exciting new features and improvements in Vue.js 3.",
                    userImage:
                        "https://images.unsplash.com/photo-1544005313-94ddf0286df2?w=100&h=100&fit=crop",
                    author: "Jane Doe",
                    readTime: "4 min Read",
                },
                {
                    image:
                        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSRPofK1humKn9zXHsNUgNA5RlEyXiqomzn2w&s",
                    title: "Advanced Tailwind Techniques",
                    description:
                        "Take your Tailwind CSS skills to the next level with these tips.",
                    userImage:
                        "https://images.unsplash.com/photo-1511367461989-f85a21fda167?w=100&h=100&fit=crop",
                    author: "John Smith",
                    readTime: "3 min Read",
                },
            ],
        };
    },
};
</script>
<style lang="">

</style>