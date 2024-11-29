<template lang="">
  <div class="max-w-[85rem] fixed top-0 z-[4] w-full mx-auto shadow-xl px-8 py-4 flex rounded-[30px] bg-white/5 shadow-[#0000004D] backdrop-blur-[100px] items-center gap-2 justify-between">
    <h1 class="font-semibold text-2xl">Kainchi</h1>
    <div class="relative w-[75%] text-[#A29E9E]">
      <input placeholder="Search in Kainchi" class="rounded-[10px] text-[#212121] w-full placeholder:text-[#A29E9E] pr-28 outline-none pl-12 py-3 shadow-lg shadow-[#0000001A] bg-white" type="text" />
      <div class="absolute left-4 top-1/2 -translate-y-1/2">
        <svg class="size-5" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" fill-rule="evenodd" d="M10.44 2.75a7.69 7.69 0 1 0 4.615 13.842c.058.17.154.329.29.464l3.84 3.84a1.21 1.21 0 0 0 1.71-1.712l-3.84-3.84a1.2 1.2 0 0 0-.463-.289A7.69 7.69 0 0 0 10.44 2.75m-5.75 7.69a5.75 5.75 0 1 1 11.5 0a5.75 5.75 0 0 1-11.5 0" clip-rule="evenodd"/></svg>
      </div>
      <div class="absolute flex items-center gap-2 cursor-pointer border-l pl-4 border-[] right-4 top-1/2 -translate-y-1/2" @click="toggleDropdown">
        <h3 class="sm:text-[18px]">Filter</h3>
        <svg class="size-5" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="m12.37 15.835l6.43-6.63C19.201 8.79 18.958 8 18.43 8H5.57c-.528 0-.771.79-.37 1.205l6.43 6.63c.213.22.527.22.74 0"/></svg>
        <div v-if="showDropdown" class="absolute top-10 right-0 z-[8] mt-2 bg-white shadow-lg rounded-lg p-4 w-48">
    <ul>
      <li><a href="#" class="block text-sm text-gray-700 hover:text-gray-900">Option 1</a></li>
      <li><a href="#" class="block text-sm text-gray-700 hover:text-gray-900">Option 2</a></li>
      <li><a href="#" class="block text-sm text-gray-700 hover:text-gray-900">Option 3</a></li>
    </ul>
  </div>
      </div>
    </div>
    <div class="flex text-[#212121] items-center gap-4">
      <div class="relative cursor-pointer">
        <svg class="size-5" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"><path d="M21.25 7.506v6.607a3.963 3.963 0 0 1-3.964 3.965h-2.643l-2.18 2.18a.636.636 0 0 1-.925 0l-2.18-2.18H6.713a3.964 3.964 0 0 1-3.964-3.965V7.506a3.964 3.964 0 0 1 3.964-3.964h10.572a3.964 3.964 0 0 1 3.964 3.964"/><path d="M12 11.338a.66.66 0 1 0 0-1.321a.66.66 0 0 0 0 1.321m4.625 0a.66.66 0 1 0 0-1.321a.66.66 0 0 0 0 1.321m-9.25 0a.66.66 0 1 0 0-1.321a.66.66 0 0 0 0 1.321"/></g></svg>
        <div class="size-2 bg-[#FF4444] rounded-full absolute top-[2px] translate-x-1/2 -translate-y-1/2 right-[2px]"></div>
      </div>
      <svg class="size-5 cursor-pointer" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 16 16"><g fill="none" stroke="currentColor"><path d="m13.258 8.354l.904.805a.91.91 0 0 1 .196 1.169l-1.09 1.862a.94.94 0 0 1-.35.341a1 1 0 0 1-.478.125a1 1 0 0 1-.306-.046l-1.157-.382q-.304.195-.632.349l-.243 1.173a.93.93 0 0 1-.339.544a.97.97 0 0 1-.618.206H6.888a.97.97 0 0 1-.618-.206a.93.93 0 0 1-.338-.544l-.244-1.173a6 6 0 0 1-.627-.35L3.9 12.61a1 1 0 0 1-.306.046a1 1 0 0 1-.477-.125a.94.94 0 0 1-.35-.34l-1.129-1.863a.91.91 0 0 1 .196-1.187L2.737 8v-.354l-.904-.805a.91.91 0 0 1-.196-1.169L2.766 3.81a.94.94 0 0 1 .35-.341a1 1 0 0 1 .477-.125a1 1 0 0 1 .306.028l1.138.4q.305-.195.632-.349l.244-1.173a.93.93 0 0 1 .338-.544a.97.97 0 0 1 .618-.206h2.238a.97.97 0 0 1 .618.206c.175.137.295.33.338.544l.244 1.173q.325.155.627.35l1.162-.382a.98.98 0 0 1 .784.078c.145.082.265.2.35.34l1.128 1.863a.91.91 0 0 1-.182 1.187l-.918.782z"/><path d="M10.5 8a2.5 2.5 0 1 1-5 0a2.5 2.5 0 0 1 5 0Z"/></g></svg>
      <img class="size-10 cursor-pointer rounded-full object-cover" src="https://thefader-res.cloudinary.com/private_images/c_limit,w_1024/c_crop,h_533,w_1024,x_0,y_73,f_auto,q_auto:eco/iwussu1yrp4nlpml4efa/iwussu1yrp4nlpml4efa.jpg" />
    </div>
  
  </div>

  <!-- Dropdown Menu -->

</template>

<script>
export default {
  data() {
    return {
      showDropdown: false, // Controls the visibility of the dropdown
    };
  },
  methods: {
    toggleDropdown() {
      this.showDropdown = !this.showDropdown; // Toggle dropdown visibility
    },
  },
};
</script>

<style lang="">
/* Add custom styles if needed */
</style>
