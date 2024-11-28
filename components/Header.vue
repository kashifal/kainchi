<template>
    <header class="relative z-[4]  py-2">
      <navbar class="mt-[100px]">
        <nav class="mx-auto max-w-7xl py-4 flex items-center justify-between px-4">
          <div class="logo flex items-center gap-2">
            <!-- Menu Icon -->
            <div class="md:hidden cursor-pointer block" @click="toggleDrawer">
              <svg
                class="size-6"
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
                  stroke-width="2"
                  d="M3 17h18M3 12h18M3 7h18"
                />
              </svg>
            </div>
            <h1 class="text-[1.5rem] font-bold">Kainchi</h1>
          </div>
  
          <!-- Desktop Links -->
          <div class="gap-5 hidden lg:flex justify-around text-[12px]">
            <a href="./#" class="active-link border-b w-fit py-1 border-black">ACCUEIL</a>
            <a href="./#" class="link hover:active-link border-b py-1 w-fit border-transparent hover:border-black">A PROPOS</a>
            <a href="./#" class="link hover:active-link border-b py-1 w-fit border-transparent hover:border-black">EXPERTISE</a>
            <a href="./#" class="link hover:active-link border-b py-1 w-fit border-transparent hover:border-black">MARQUES & PRODUITS</a>
            <a href="./#" class="link hover:active-link border-b py-1 w-fit border-transparent hover:border-black">MARQUE PRIVEE</a>
            <a href="./#" class="link hover:active-link border-b py-1 w-fit border-transparent hover:border-black">CONTACT</a>
          </div>
  
          <!-- Account -->
          <div
            class="items-center h-fit text-[#212121] py-1 px-3 flex cursor-pointer justify-center rounded-full border-[1px] border-[#DBDBDB] bg-[#DBDBDB]"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="size-5"
              width="1em"
              height="1em"
              viewBox="0 0 24 24"
            >
              <path
                fill="currentColor"
                d="M12 4a4 4 0 0 1 4 4a4 4 0 0 1-4 4a4 4 0 0 1-4-4a4 4 0 0 1 4-4m0 2a2 2 0 0 0-2 2a2 2 0 0 0 2 2a2 2 0 0 0 2-2a2 2 0 0 0-2-2m0 7c2.67 0 8 1.33 8 4v3H4v-3c0-2.67 5.33-4 8-4m0 1.9c-2.97 0-6.1 1.46-6.1 2.1v1.1h12.2V17c0-.64-3.13-2.1-6.1-2.1"
              />
            </svg>
            <p>My Account</p>
          </div>
        </nav>
      </navbar>
  
      <!-- Drawer -->
      <transition name="slide">
        <div
          v-show="drawerOpen"
          class="fixed lg:hidden flex inset-0 bg-white text-[#212121] z-[5]"
        >
          <div class="absolute cursor-pointer top-5 right-5" @click="toggleDrawer">
            <svg
              class="size-10"
              xmlns="http://www.w3.org/2000/svg"
              width="1em"
              height="1em"
              viewBox="0 0 16 16"
            >
              <path
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="1.5"
                d="m11.25 4.75l-6.5 6.5m0-6.5l6.5 6.5"
              />
            </svg>
          </div>
          <div class="flex w-full text-left flex-col gap-5 px-6 justify-center items-start text-xl h-full">
            <a href="./#" class="active-link border-b w-fit border-black py-1">ACCUEIL</a>
            <a href="./#" class="link hover:active-link py-1 border-b w-fit border-transparent hover:border-black">A PROPOS</a>
            <a href="./#" class="link hover:active-link py-1 border-b w-fit border-transparent hover:border-black">EXPERTISE</a>
            <a href="./#" class="link hover:active-link py-1 border-b w-fit border-transparent hover:border-black">MARQUES & PRODUITS</a>
            <a href="./#" class="link hover:active-link py-1 border-b w-fit border-transparent hover:border-black">MARQUE PRIVEE</a>
            <a href="./#" class="link hover:active-link py-1 border-b w-fit border-transparent hover:border-black">CONTACT</a>
          </div>
        </div>
      </transition>
    </header>
  </template>
  
  
  <script setup>
  import { ref } from "vue";
  
  const drawerOpen = ref(false);
  
  function toggleDrawer() {
    drawerOpen.value = !drawerOpen.value;
  }
  </script>
  
  <style>
  /* Transition styles */
  /* Transition styles */
.slide-enter-active,
.slide-leave-active {
  transition: transform 0.5s ease;
}
.slide-enter-from {
  transform: translateX(-100%);
}
.slide-leave-to {
  transform: translateX(-100%);
}

  </style>
  