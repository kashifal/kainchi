<template lang="">
     <main class="flex-1 xl:pl-[19rem] min-h-screen h-full px-8 pt-28 pb-20 rounded-lg  bg-[#E3E3E5]">
        <div class="backdrop-blur-sm h-[90vh] overflow-auto bg-opacity-20 p-6 rounded-3xl border bg-white border-white/20 shadow-lg custom-scrollbar">
            <div class="mb-8 ">
                <h2 class="text-[1.5rem] font-bold text-gray-800">Hello Webmaster, Welcome to Kain'chi</h2>
                <div class="flex bg-[#E9E9EE]/50 backdrop-blur-sm py-[6px] pl-[10px] rounded-lg mt-[20px]">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2L9.19 8.63L2 9.24l5.46 4.73L5.82 21z"/></svg>
                    <p class="text-gray-600 ml-[10px]">
                        Before you start using Kainchi, we suggest you
                        <a href="#" class="text-purple-600 hover:underline">Watch this demo.</a>
                    </p>
                </div>
            </div>
            
            <div class="grid grid-cols-1 gap-6 mb-8 sm:grid-cols-2 lg:grid-cols-4">
                
                <div class="p-2 bg-white rounded-lg shadow">
                    <h3 class="text-[18px] font-bold text-gray-800 pl-[6px]">300</h3>
                    <p class="text-gray-500 pl-[6px]">Total Profiles</p>
                    <div class="flex mt-[50px] pl-[6px]">
                        <!-- <img src="./foundation--graph-bar.svg" class="w-[26px]" alt=""> -->
                        <p class="mt-2 text-sm font-medium text-green-600">+125%</p>
                    </div>
                </div>

                <div class="p-2 bg-white rounded-lg shadow">
          <h3 class="text-[18px] font-bold text-gray-800 pl-[6px]">205</h3>
          <p class="text-gray-500 pl-[6px]">Account Balance</p>
          <div class="flex mt-[50px] pl-[6px]">
            <!-- <img src="./foundation--graph-bar.svg" class="w-[26px]" alt=""> -->
          <p class="mt-2 text-sm font-medium text-green-600">+50%</p>
        </div>
        </div>
        
        <div class="p-2 bg-white rounded-lg shadow">
            <h3 class="text-[18px] font-bold text-gray-800 pl-[6px] ">456</h3>
            <p class="text-gray-500 pl-[6px]">New Sales</p>
            <div class="flex mt-[50px] pl-[6px]">
              <!-- <img src="./foundation--graph-bar.svg" class="w-[26px]" alt=""> -->
            <p class="mt-2 text-sm font-medium text-red-600">-12%</p>
          </div>
          </div>
          <div class="p-2 bg-white rounded-lg shadow">
              <h3 class="text-[18px] font-bold text-gray-800 pl-[6px]">12</h3>
              <p class="text-gray-500 pl-[6px]">Pending Contacts</p>
              <div class="flex mt-[50px] pl-[6px]">
                <!-- <img src="./foundation--graph-bar.svg" class="w-[26px]" alt=""> -->
              <p class="mt-2 text-sm font-medium text-green-600">+29%</p>
            </div>
            </div>
                
            </div>

            
            <div>
                <h3 class="mb-6 text-xl font-bold text-gray-800">Overview</h3>
                <div class="grid grid-cols-1 gap-6 sm:grid-cols-2">
                    
                    <div class="p-6 bg-white rounded-lg shadow">
                        <h4 class="mb-4 text-lg font-medium text-gray-600">Revenue <span class="text-[#92EBC2]">(1,038 Visits)</span></h4>
                        <div class="h-32 rounded-lg bg-gray-50"></div> 
                    </div>
                    
                    <div class="p-6 bg-white rounded-lg shadow">
                        <h4 class="mb-4 text-lg font-medium text-gray-600">Traffic <span class="text-[#92EBC2]">(1,230 Visits)</span></h4>
                        <div class="h-32 rounded-lg bg-gray-50"></div> 
                    </div>
                </div>
            </div>
        </div>
        </main>
</template>
<script>

</script>
<style lang="css">
.custom-scrollbar::-webkit-scrollbar {
    width: 6px;
}

.custom-scrollbar::-webkit-scrollbar-track {
    background: rgba(255, 255, 255, 0.1);
    border-radius: 10px;
    backdrop-filter: blur(5px);
}

.custom-scrollbar::-webkit-scrollbar-thumb {
    background: rgba(255, 255, 255, 0.4);
    border-radius: 10px;
    backdrop-filter: blur(5px);
    border: 1px solid rgba(255, 255, 255, 0.2);
}

.custom-scrollbar::-webkit-scrollbar-thumb:hover {
    background: rgba(255, 255, 255, 0.5);
}

/* For Firefox */
.custom-scrollbar {
    scrollbar-width: thin;
    scrollbar-color: rgba(255, 255, 255, 0.4) rgba(255, 255, 255, 0.1);
}
</style>