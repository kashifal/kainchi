<template lang="">
    <div>
        <div class="flex  px-4 min-h-screen items-center justify-center bg-gray-100">
        <div class="flex w-full max-w-xl h-[95vh] lg:max-w-4xl overflow-hidden bg-white shadow-lg">
          
          <div class="flex-1 px-4 sm:px-8 py-4 text-center ">

            <div class=" flex ">
                <!-- <img src="./tdesign--letters-k white.svg" class="h-[40px] invert " alt=""> -->
                <p class="text-[18px] text-black tracking-wider font-semibold mt-[7px] ml-[0px]">Kainchi</p>
            </div>
            <h1 class="text-2xl font-bold text-gray-800">Welcome</h1>
            <p class="mt-2 text-sm text-gray-600">Welcome back! Please enter your details</p>
      
            <div class="mt-6">
              <button class="flex w-full items-center justify-center space-x-2 rounded-lg border border-gray-300 bg-white py-2 px-4 text-sm font-medium text-gray-700 shadow-sm hover:bg-gray-50">
                <img src="https://www.google.com/favicon.ico" alt="Google" class="h-5 w-5">
                <span>Log in with Google</span>
              </button>
            </div>
      
            <div class="my-6 flex items-center">
              <div class="flex-1 border-t border-gray-300"></div>
              <p class="px-4 text-sm text-gray-600">or</p>
              <div class="flex-1 border-t border-gray-300"></div>
            </div>
      
            <form action="#" class="space-y-4">
              <div>
                
                <input id="email" type="email" placeholder="Email" class="w-full bg-transparent  border-b-[1px] border-gray-400 px-4 py-2 text-sm outline-none ">
              </div>
      
              <div>
                
                <input id="password" type="password" placeholder="Password"  class="w-full bg-transparent  border-b-[1px] border-gray-400 px-4 py-2 text-sm outline-none ">
              </div>
      
              <div class="flex flex-wrap items-center justify-between text-sm">
                <label class="flex  items-center space-x-2">
                  <input type="checkbox" class="rounded border-gray-300 text-indigo-600 focus:ring-indigo-500">
                  <span class="text-[13px] font-medium">Remember for 30 days</span>
                </label>
                <a href="#" class="text-black text-[13px] underline">Forgot password</a>
              </div>
      
              <button class="w-full mt-4 rounded-lg bg-[#212121] py-2.5 text-sm font-medium text-white hover:bg-black/90">Log in</button>
            </form>
      
            <p class="mt-6 text-center text-sm text-black">
              Don’t have an account?
              <a href="#" class="font-semibold hover:underline">Sign up for free</a>
            </p>
          </div>
      
          <div :style="{
               backgroundImage: `linear-gradient(to bottom right, rgb(147, 51, 234), rgb(168, 85, 247), rgb(107, 33, 168)), url('${slides[currentSlide].image}')`,
               backgroundSize: 'cover',
               backgroundBlendMode: 'overlay'
           }" 
               class="hidden mx-4 my-4 rounded-3xl w-1/2 p-8 text-white lg:flex lg:flex-col lg:justify-between">
            <div>
              <p class="text-[1.4rem] font-bold mt-[240px]">{{ slides[currentSlide].heading }}</p>
            </div>
      
            <div class="mt-auto flex items-center justify-between">
              <div>
                <p class="text-lg font-semibold">{{ slides[currentSlide].author }}</p>
                <p class="text-sm">{{ slides[currentSlide].role }}</p>
              </div>

              <div class="">
                <div class="flex items-center space-x-[2px]">
                  <template v-for="n in 5" :key="n">
                    <svg :class="n <= slides[currentSlide].rating ? 'text-white' : 'text-gray-300'" 
                         xmlns="http://www.w3.org/2000/svg" class="cursor-pointer size-4" width="1em" height="1em" viewBox="0 0 24 24">
                      <path fill="currentColor" fill-rule="evenodd" d="M12.908 1.581a1 1 0 0 0-1.816 0l-2.87 6.22l-6.801.807a1 1 0 0 0-.562 1.727l5.03 4.65l-1.335 6.72a1 1 0 0 0 1.469 1.067L12 19.426l5.977 3.346a1 1 0 0 0 1.47-1.068l-1.335-6.718l5.029-4.651a1 1 0 0 0-.562-1.727L15.777 7.8z" clip-rule="evenodd"/>
                    </svg>
                  </template>
                </div>
                <div class="flex gap-2 mt-8">
                          <div @click="prevSlide" class="size-[50px] rounded-full flex items-center justify-center cursor-pointer hover:bg-[#212121] hover:text-white border border-[#212121] ">
                            <svg class="size-8" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="M10.733 19.79a.75.75 0 0 0 1.034-1.086L5.516 12.75H20.25a.75.75 0 0 0 0-1.5H5.516l6.251-5.955a.75.75 0 0 0-1.034-1.086l-7.42 7.067a1 1 0 0 0-.3.58a.8.8 0 0 0 .001.289a1 1 0 0 0 .3.579z"/></svg>
                          </div>
                          <div @click="nextSlide" class="size-[50px] rotate-180 rounded-full flex items-center justify-center cursor-pointer hover:bg-[#212121] hover:text-white border border-[#212121] ">
                            <svg class="size-8" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="M10.733 19.79a.75.75 0 0 0 1.034-1.086L5.516 12.75H20.25a.75.75 0 0 0 0-1.5H5.516l6.251-5.955a.75.75 0 0 0-1.034-1.086l-7.42 7.067a1 1 0 0 0-.3.58a.8.8 0 0 0 .001.289a1 1 0 0 0 .3.579z"/></svg>
                          </div>
                        </div>
            </div>
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
            currentSlide: 0,
            slides: [
                {
                    image: 'https://img.freepik.com/premium-photo/portrait-young-woman-professional-football-player-motion-isolated-purple-background-neon_155003-45609.jpg',
                    heading: 'The e-commerce revolution in Morocco has been growing rapidly in recent years, with more and more ...',
                    author: 'Hamza',
                    role: 'SEO Kainchi Agency',
                    rating: 3
                },
                {
                    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRLcC2GMVRJzFZUEA3YuortzBkYtly7S96J9Q&s',
                    heading: 'Digital transformation is reshaping the way businesses operate in the modern era...',
                    author: 'Sarah',
                    role: 'Digital Strategist',
                    rating: 8
                },
                   {
                    image: 'https://i.ytimg.com/vi/Gf88wMYf8IY/hqdefault.jpg',
                    heading: 'Digital transformation is reshaping the way businesses operate in the modern era...',
                    author: 'Sarah',
                    role: 'Digital Strategist',
                    rating: 7
                },
                {
                    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSnb9INrHOTGafLQ3ZuUdZqo2rRi_KiCFFZaw&s',
                    heading: 'Innovation and technology are driving sustainable growth across industries...',
                    author: 'Ahmed',
                    role: 'Tech Lead',
                    rating: 6
                }
            ]
        }
    },
    methods: {
        nextSlide() {
            this.currentSlide = (this.currentSlide + 1) % this.slides.length
        },
        prevSlide() {
            this.currentSlide = (this.currentSlide - 1 + this.slides.length) % this.slides.length
        }
    }
}
</script>
<style lang="">
    
</style>