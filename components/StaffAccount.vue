<template lang="">
    <div>
        <main class="flex-1 px-6 pt-2 rounded-lg">
            <!-- Header -->
            <header class="mb-8">
                <p class="text-sm text-[#D2D2D2]">Dashboard > Profiles > New</p>
                <h1 class="text-2xl font-bold text-gray-700 mt-2">Staff Accounts</h1>
            </header>
        
            <!-- Content Section -->
            <div class="flex flex-col lg:flex-row space-y-6 lg:space-y-0 lg:space-x-8 bg-white rounded-lg p-6">
                <!-- Left Section -->
                <div class="flex-1">
                    <!-- Image Section -->
                    <div class="flex justify-center mt-8 lg:mt-24">
                        <img src="./ci--image-02.svg" class="h-10" alt="Illustration">
                    </div>
                    <!-- Text Content -->
                    <div class="mt-[270px] p-4 rounded-lg border-2">
                        <p class="font-bold text-lg">Understanding various categories in Kainchi</p>
                        <p class="text-sm text-gray-600 mt-4 leading-relaxed">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Veniam non velit obcaecati. Lorem ipsum dolor sit amet consectetur adipisicing elit. Non velit obcaecati adipisci.
                        </p>
                    </div>
                </div>
        
                <!-- Right Section -->
                <div class="w-full lg:w-1/2 p-4 lg:p-6">
                    <h2 class="text-[1.5rem] font-semibold text-gray-700">Add new staff members easily!</h2>
                    <p class="text-sm font-medium text-[#7A797D]">Categories</p>
        
                    <form class="space-y-6 mt-4">
                        <!-- Full Name Input -->
                        <div>
                            <label for="name" class="block text-sm font-semibold text-gray-700">Full Name</label>
                            <input
                                type="text"
                                id="name"
                                class="w-full px-4 py-3 mt-2 border rounded-md bg-white focus:outline-none focus:ring focus:ring-indigo-300  bg-gradient-to-r from-purple-100 to-purple-200 shadow-md rounded-lg"
                                placeholder="">
                        </div>
        
                        <!-- Email Input -->
                        <div>
                            <label for="email" class="block text-sm font-semibold text-gray-700">E-mail</label>
                            <input
                                type="email"
                                id="email"
                                class="w-full px-4 py-3 mt-2 border rounded-md bg-white focus:outline-none focus:ring focus:ring-indigo-300 bg-gradient-to-r from-purple-100 to-purple-200 shadow-md rounded-lg"
                                placeholder="">
                        </div>
        
                        <!-- Password Input -->
                        <div>
                            <label for="password" class="block text-sm font-semibold text-gray-700">Password</label>
                            <input
                                type="password"
                                id="password"
                                class="w-full px-4 py-3 mt-2 border rounded-md bg-white focus:outline-none focus:ring focus:ring-indigo-300 bg-gradient-to-r from-purple-100 to-purple-200 shadow-md rounded-lg"
                                placeholder="">
                        </div>
        
                        <!-- Profile Type Input -->
                        <div>
                            <label for="profile-type" class="block text-sm font-semibold text-gray-700">Profile Type</label>
                            <input
                                type="text"
                                id="profile-type"
                                class="w-full px-4 py-3 mt-2 border rounded-md bg-white focus:outline-none focus:ring focus:ring-indigo-300 bg-gradient-to-r from-purple-100 to-purple-200 shadow-md rounded-lg"
                                placeholder="">
                        </div>
        
                        <!-- Submit Button -->
                        <button
                            type="submit"
                            class="w-full bg-indigo-600 text-white py-3 rounded-full hover:bg-indigo-500 focus:outline-none focus:ring-2 focus:ring-indigo-400">
                            Create Account
                        </button>
                    </form>
                </div>
            </div>
        </main>
    </div>
</template>
<script>
export default {
    
}
</script>
<style lang="">
    
</style>