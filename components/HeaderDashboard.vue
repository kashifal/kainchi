<template lang="">
  <div class=" mx-auto fixed top-0 z-[4] w-full mx-auto shadow-md px-4 sm:px-8 py-4 flex rounded-[30px] bg-white/5 shadow-[#0000004D]/10 backdrop-blur-[100px] items-center gap-2 justify-between">
    <div class="flex items-center gap-2">
    <button @click="$emit('update:modelValue', !modelValue)" class="xl:hidden p-2 rounded-lg hover:bg-white/10">
      <svg class="size-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
      </svg>
    </button>
    <h1 class="font-semibold text-xl sm:text-2xl">Kainchi</h1>
  </div>
    <div class="hidden md:relative md:block w-[75%] text-[#A29E9E]">
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
    
    <div class="flex text-[#212121]  items-center gap-3">
      <button @click="toggleSearch" class="md:hidden p-1.5 bg-opacity-50 hover:bg-gray-100 backdrop-blur-3xl rounded-full">
      <svg class="size-5" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
      </svg>
    </button>
      <div class="p-1.5 bg-opacity-50 backdrop-blur-3xl rounded-full hover:bg-gray-100">
        <div class="relative cursor-pointer" @click="toggleNotifications">
          <svg class="size-5" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"><path d="M21.25 7.506v6.607a3.963 3.963 0 0 1-3.964 3.965h-2.643l-2.18 2.18a.636.636 0 0 1-.925 0l-2.18-2.18H6.713a3.964 3.964 0 0 1-3.964-3.965V7.506a3.964 3.964 0 0 1 3.964-3.964h10.572a3.964 3.964 0 0 1 3.964 3.964"/><path d="M12 11.338a.66.66 0 1 0 0-1.321a.66.66 0 0 0 0 1.321m4.625 0a.66.66 0 1 0 0-1.321a.66.66 0 0 0 0 1.321m-9.25 0a.66.66 0 1 0 0-1.321a.66.66 0 0 0 0 1.321"/></g></svg>
          <div class="size-2 bg-[#FF4444] rounded-full absolute top-[2px] translate-x-1/2 -translate-y-1/2 right-[2px]"></div>
        </div>
      </div>
      <div v-if="showNotifications" class="absolute w-full sm:w-auto right-0 top-20 z-50">
        <div class="sm:w-80 w-[100%] bg-gray-100 rounded-3xl shadow-lg p-4">
          <!-- Notifications Header -->
          <h2 class="text-lg font-semibold py-3 bg-white   -mt-4 w-[112%] -ml-4 shadow-2xl shadow-neutral-300 text-center p-2 rounded-full text-gray-800 mb-4">Notifications</h2>
          <!-- Notification Items -->
          <div class="space-y-4">
            <!-- Notification Item -->
            <div class="flex items-center">
              <img src="https://clipground.com/images/licking-ice-cream-clipart-6.jpg" alt="User" class="w-10 object-cover h-10 rounded-full mr-4">
              <div>
                <p class="text-sm text-gray-800">
                  <span class="font-semibold">David Lee</span> sent you a message.
                </p>
                <p class="text-xs text-gray-500">4 min ago</p>
              </div>
            </div>

            <div class="flex items-center">
              <img src="https://th.bing.com/th/id/OIP.28woZ3gvcoHpZ9LnQHBghAHaPL?w=976&h=2000&rs=1&pid=ImgDetMain" alt="User" class="w-10 object-cover h-10 rounded-full mr-4">
              <div>
                <p class="text-sm text-gray-800">
                  <span class="font-semibold">Alex Johnson</span> sent you a message.
                </p>
                <p class="text-xs text-gray-500">4 min ago</p>
              </div>
            </div>

            <div class="flex items-center">
              <img src="https://th.bing.com/th/id/OIP.aDEQtGy5KZ6aP8awDOsOLAHaUK?w=705&h=1920&rs=1&pid=ImgDetMain" alt="User" class="w-10 object-cover h-10 rounded-full mr-4">
              <div>
                <p class="text-sm text-gray-800">
                  <span class="font-semibold">Jonathan Chen</span> sent you mail.
                </p>
                <p class="text-xs text-gray-500">4 min ago</p>
              </div>
            </div>

            <div class="flex items-center">
              <img src="https://img.freepik.com/premium-vector/cute-little-boy-with-ice-cream_50699-459.jpg?w=1380" alt="User" class="w-10 object-cover h-10 rounded-full mr-4">
              <div>
                <p class="text-sm text-gray-800">
                  <span class="font-semibold">Robert Grant</span> sent you mail.
                </p>
                <p class="text-xs text-gray-500">4 min ago</p>
              </div>
            </div>

            <div class="flex items-center">
              <img src="https://th.bing.com/th/id/OIP.ZxSGFd93977Sp3ffSSwkJAAAAA?w=474&h=798&rs=1&pid=ImgDetMain" alt="User" class="w-10 object-cover h-10 rounded-full mr-4">
              <div>
                <p class="text-sm text-gray-800">
                  <span class="font-semibold">David James</span> sent you mail.
                </p>
                <p class="text-xs text-gray-500">4 min ago</p>
              </div>
            </div>
          </div>
          <!-- View All Link -->
          <div class="mt-4 text-center">
            <a href="#" class="text-sm text-indigo-600 hover:underline">View all notifications</a>
          </div>
        </div>
      </div>
      <div class="p-1.5 bg-opacity-50 backdrop-blur-3xl rounded-full rounded-full hover:bg-gray-100">
      
      <svg class="size-5 cursor-pointer" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 16 16"><g fill="none" stroke="currentColor"><path d="m13.258 8.354l.904.805a.91.91 0 0 1 .196 1.169l-1.09 1.862a.94.94 0 0 1-.35.341a1 1 0 0 1-.478.125a1 1 0 0 1-.306-.046l-1.157-.382q-.304.195-.632.349l-.243 1.173a.93.93 0 0 1-.339.544a.97.97 0 0 1-.618.206H6.888a.97.97 0 0 1-.618-.206a.93.93 0 0 1-.338-.544l-.244-1.173a6 6 0 0 1-.627-.35L3.9 12.61a1 1 0 0 1-.306.046a1 1 0 0 1-.477-.125a.94.94 0 0 1-.35-.34l-1.129-1.863a.91.91 0 0 1 .196-1.187L2.737 8v-.354l-.904-.805a.91.91 0 0 1-.196-1.169L2.766 3.81a.94.94 0 0 1 .35-.341a1 1 0 0 1 .477-.125a1 1 0 0 1 .306.028l1.138.4q.305-.195.632-.349l.244-1.173a.93.93 0 0 1 .338-.544a.97.97 0 0 1 .618-.206h2.238a.97.97 0 0 1 .618.206c.175.137.295.33.338.544l.244 1.173q.325.155.627.35l1.162-.382a.98.98 0 0 1 .784.078c.145.082.265.2.35.34l1.128 1.863a.91.91 0 0 1-.182 1.187l-.918.782z"/><path d="M10.5 8a2.5 2.5 0 1 1-5 0a2.5 2.5 0 0 1 5 0Z"/></g></svg>
      </div>
      <img class="size-10 cursor-pointer rounded-full object-cover" src="https://thefader-res.cloudinary.com/private_images/c_limit,w_1024/c_crop,h_533,w_1024,x_0,y_73,f_auto,q_auto:eco/iwussu1yrp4nlpml4efa/iwussu1yrp4nlpml4efa.jpg" />
    </div>
  
  </div>

  <div v-if="showMobileSearch" class="fixed inset-0 z-50 bg-white p-4">
    <div class="relative">
      <input placeholder="Search in Kainchi" class="w-full rounded-[10px] text-[#212121] placeholder:text-[#A29E9E] pr-12 outline-none pl-12 py-3 shadow-lg shadow-[#0000001A] bg-white" type="text" />
      <button @click="toggleSearch" class="absolute right-4 top-1/2 -translate-y-1/2">
        <svg class="size-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>
  </div>



  <div class="absolute hidden w-full max-w-sm p-4 bg-white rounded-2xl shadow-lg">
    <!-- Icon -->
    <div class="flex items-center">
      <div class="w-8 h-8 flex items-center justify-center bg-purple-100 text-purple-600 rounded-full">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5">
          <path stroke-linecap="round" stroke-linejoin="round" d="M13.875 18.825a4.5 4.5 0 01-7.5 0M14.1 8.237a4.5 4.5 0 10-6.1 6.1M20.33 17.33a4.5 4.5 0 01-4.5-4.5M8.567 5.567a4.5 4.5 0 015.1-1.33" />
        </svg>
      </div>
      <h3 class="ml-3 text-lg font-semibold text-gray-800">Notifications</h3>
    </div>
    <!-- Close Button -->
    <button class="absolute top-3 right-3 text-gray-400 hover:text-gray-600">
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5">
        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
      </svg>
    </button>
    <!-- Text -->
    <p class="mt-3 text-sm text-gray-600 leading-relaxed">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque pretium mauris lectus, ac mattis eros pulvinar a. Donec ac.
    </p>
  </div>

  <Transition name="notification">
    <div v-if="showToast" 
         class="fixed bottom-4 z-[9999999999999999999999999999999999999999999999999999999999999999999999] right-4 w-full max-w-sm p-4 bg-white rounded-2xl shadow-lg transform-gpu animate-notification"
         @click="dismissNotification">
      <div class="flex items-center">
        <div class="w-8 h-8 flex items-center justify-center bg-purple-100 text-purple-600 rounded-full">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-5 h-5">
            <path stroke-linecap="round" stroke-linejoin="round" d="M13.875 18.825a4.5 4.5 0 01-7.5 0M14.1 8.237a4.5 4.5 0 10-6.1 6.1M20.33 17.33a4.5 4.5 0 01-4.5-4.5M8.567 5.567a4.5 4.5 0 015.1-1.33" />
          </svg>
        </div>
        <h3 class="ml-3 text-lg font-semibold text-gray-800">New Notification!</h3>
      </div>
      <p class="mt-3 text-sm text-gray-600 leading-relaxed">
        {{ currentNotification }}
      </p>
    </div>
  </Transition>

</template>

<script>
import SideBarDashboard from './SideBarDashboard.vue'

export default {
 
  data() {
    return {
      showDropdown: false,
      showMobileSearch: false,
      isSidebarOpen: false,
      showNotifications: false,
      showToast: false,
      currentNotification: '',
      lastNotification: '',
      notifications: [
        'New message from Kashif Sulehri',
        'Shaheer Sulehri commented on your post',
        'Sanwal Sulehri reminder in 30 minutes',
        'You have a new follower',
        'Your report is ready to view',
      ],
      notificationInterval: null
    };
  },
  methods: {
    toggleDropdown() {
      this.showDropdown = !this.showDropdown;
    },
    toggleSearch() {
      this.showMobileSearch = !this.showMobileSearch;
    },
    toggleNotifications() {
      this.showNotifications = !this.showNotifications;
    },
    showRandomNotification() {
      let newNotification;
      do {
        newNotification = this.notifications[Math.floor(Math.random() * this.notifications.length)];
      } while (newNotification === this.lastNotification && this.notifications.length > 1);
      
      this.lastNotification = newNotification;
      this.currentNotification = newNotification;
      this.showToast = true;
      
      setTimeout(() => {
        this.showToast = false;
      }, 5000);
    },
    dismissNotification() {
      this.showToast = false;
    }
  },
  mounted() {
    // Show notification every 5 seconds instead of 120 seconds
    this.notificationInterval = setInterval(() => {
      this.showRandomNotification();
    }, 5000);
  },
  beforeUnmount() {
    // Clean up interval
    clearInterval(this.notificationInterval);
  },
  props: {
    modelValue: {
      type: Boolean,
      default: false
    }
  }
};
</script>
<style scoped>
.transform {
  transition-property: transform;
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  transition-duration: 300ms;
}

.notification-enter-active,
.notification-leave-active {
  transition: all 0.5s ease;
}

.notification-enter-from {
  opacity: 0;
  transform: translateX(100%) scale(0.5);
}

.notification-leave-to {
  opacity: 0;
  transform: translateX(100%) scale(0.9);
}

@keyframes notification-bounce {
  0% { transform: translateX(100%) scale(0.5); }
  50% { transform: translateX(-20px) scale(1.05); }
  75% { transform: translateX(10px) scale(0.95); }
  100% { transform: translateX(0) scale(1); }
}

.animate-notification {
  animation: notification-bounce 0.8s ease-out;
}
</style>

