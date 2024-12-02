<template lang="">
    <div class="bg-[url('https://img.freepik.com/premium-photo/mobile-phone-hand-purple-background-with-sample-home-screen-icons-screen_746318-434.jpg')] bg-cover bg-center min-h-screen w-full">
        <!-- Common wrapper div that will be reused -->
        <div class="flex items-center justify-center backdrop-blur-[100px] bg-[#573BD5]/20 min-h-screen">
            <!-- First section (Email) -->
            <div v-if="currentStep === 1" class="w-full px-4 md:px-0">
                <div class="flex flex-col items-center gap-3">
                    <div class="bg-white/90 p-8 rounded-2xl shadow-lg w-full max-w-md text-center relative">
                        <div class="absolute -top-10 left-1/2 border-4 border-[#9758C4] transform -translate-x-1/2 w-20 h-20 rounded-full bg-white shadow-md flex items-center justify-center">
                            K
                        </div>
                        <h2 class="text-xl font-semibold mt-12 mb-4">Enter your email</h2>
                        <form @submit.prevent="validateAndGoToPassword">
                            <input 
                                v-model="email" 
                                type="email" 
                                placeholder="Enter your email" 
                                :class="[
                                    'w-full p-2 border-b-2 bg-transparent focus:outline-none focus:border-indigo-500 mb-6 transition-all duration-300',
                                    isHighlighted ? 'border-red-500 animate-shake' : 'border-gray-300'
                                ]"
                            />
                            <button 
                                type="submit" 
                                :class="[
                                    'w-full text-white py-3 rounded-full font-semibold transition-all duration-300',
                                    isHighlighted ? 'bg-red-500 animate-pulse' : 'bg-black hover:bg-gray-800'
                                ]"
                            >
                                Sign up or sign in
                            </button>
                        </form>
                        <p class="text-sm text-gray-500 mt-6">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore.
                        </p>
                    </div>
                </div>
            </div>

            <!-- Second section (Password) -->
            <div v-else-if="currentStep === 2" class="w-full px-4 md:px-0">
                <div class="flex flex-col items-center gap-3">
                    <div class="bg-white/90 p-8 rounded-2xl shadow-lg w-full max-w-md text-center relative">
                        <div class="absolute -top-10 left-1/2 border-4 border-[#9758C4] transform -translate-x-1/2 w-20 h-20 rounded-full bg-white shadow-md flex items-center justify-center">
                            K
                        </div>
                        <h2 class="text-xl font-semibold mt-12 mb-4">Enter your Password</h2>
                        <form @submit.prevent="validateAndGoToUsername">
                            <input 
                                v-model="password" 
                                type="password" 
                                placeholder="Enter your password" 
                                :class="[
                                    'w-full bg-transparent p-2 border-b-2 focus:outline-none focus:border-indigo-500 mb-6',
                                    isHighlighted ? 'border-red-500 animate-shake' : 'border-gray-300'
                                ]"
                                @input="validatePassword"
                            />
                            <button 
                                type="submit" 
                                :class="[
                                    'w-full text-white py-3 rounded-full font-semibold transition-all duration-300',
                                    isHighlighted ? 'bg-red-500 animate-pulse' : 'bg-black hover:bg-gray-800'
                                ]"
                            >
                                Sign up or sign in
                            </button>
                            <p v-if="passwordError" class="text-[12px] text-[#B41717] mt-3">
                                {{ passwordError }}
                            </p>
                        </form>
                    </div>
                </div>
            </div>

            <!-- Third section (Username) -->
            <div v-else-if="currentStep === 3" class="w-full px-4 md:px-0">
                <div class="flex flex-col items-center gap-3">
                    <div class="bg-white/90 p-8 rounded-2xl shadow-lg w-full max-w-md text-center relative">
                        <div class="absolute overflow-hidden group -top-10 left-1/2 border-4 border-[#9758C4] transform -translate-x-1/2 w-20 h-20 rounded-full bg-white shadow-md flex items-center justify-center">
                            K
                            <div class="w-full h-6 absolute bottom-0 group-hover:flex hidden group-hover:bg-gray-200  items-center justify-center">
                                <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 21 21"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M17 4a2.12 2.12 0 0 1 0 3l-9.5 9.5l-4 1l1-3.944l9.504-9.552a2.116 2.116 0 0 1 2.864-.125zM9.5 17.5h8m-2-11l1 1"/></svg>
                            </div>
                        </div>
                        <h2 class="text-xl font-semibold mt-12 mb-4">Enter your Username</h2>
                        <form @submit.prevent="validateAndSaveUsername">
                            <input 
                                v-model="username" 
                                type="email" 
                                placeholder="Enter your username" 
                                class="w-full bg-transparent  p-2 border-b-2 border-gray-300 focus:outline-none focus:border-indigo-500 mb-6" 
                            />
                            <button type="submit" class="w-full bg-black text-white py-3 rounded-full font-semibold hover:bg-gray-800 transition-colors">
                                Save
                            </button>
                            <p class="text-sm text-gray-500 mt-6">
                                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore.
                            </p>
                        </form>
                    </div>
                </div>
            </div>

            <!-- Pagination dots - moved outside steps -->
            <div class="absolute bottom-20 left-1/2 transform -translate-x-1/2 flex gap-2">
                <div 
                    v-for="step in 3" 
                    :key="step"
                    @click="handlePaginationClick(step)"
                    class="w-2.5 h-2.5 rounded-full cursor-pointer transition-all"
                    :class="[
                        currentStep === step 
                            ? 'bg-white scale-125' 
                            : 'bg-white/70 hover:bg-white/90'
                    ]"
                ></div>
            </div>

            <!-- Brand name -->
            <div class="absolute flex left-2 bottom-4">
                <p class="text-[18px] text-white tracking-wider font-semibold">Kainchi</p>
            </div>
        </div>

        <!-- Add modal for empty input warning -->
        <div v-if="showModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
            <div class="bg-white p-6 rounded-lg shadow-xl">
                <h3 class="text-xl text-red-600 font-semibold mb-2">Warning</h3>
                <p class="text-gray-600">Please fill in the required field before continuing.</p>
                <button 
                    @click="showModal = false" 
                    class="mt-4 px-4 py-2 bg-red-600 text-white rounded-full hover:bg-red-700"
                >
                    OK
                </button>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            currentStep: 1,
            email: '',
            password: '',
            username: '',
            showModal: false,
            passwordError: '',
            isHighlighted: false
        }
    },
    methods: {
        goToPassword() {
            this.currentStep = 2
        },
        goToUsername() {
            this.currentStep = 3
        },
        saveUsername() {
            // Handle saving username
        },
        validateAndGoToPassword() {
            if (!this.email.trim()) {
                this.showModal = true
                return
            }
            this.goToPassword()
        },
        validateAndGoToUsername() {
            if (!this.password.trim()) {
                this.showModal = true;
                return;
            }
            if (this.passwordError) {
                return;
            }
            this.goToUsername();
        },
        validateAndSaveUsername() {
            if (!this.username.trim()) {
                this.showModal = true
                return
            }
            this.saveUsername()
        },
        validatePassword() {
            const hasUpperCase = /[A-Z]/.test(this.password);
            const hasLowerCase = /[a-z]/.test(this.password);
            const hasNumbers = /\d/.test(this.password);
            const hasSpecialChar = /[!@#$%^&*(),.?":{}|<>]/.test(this.password);
            
            if (this.password.length < 8) {
                this.passwordError = 'Password must be at least 8 characters long';
            } else if (!hasUpperCase || !hasLowerCase || !hasNumbers || !hasSpecialChar) {
                this.passwordError = 'Password must contain uppercase, lowercase, numbers, and special characters';
            } else {
                this.passwordError = '';
            }
        },
        handlePaginationClick(step) {
            if (step === 1) {
                this.currentStep = 1;
            } else if (step === 2) {
                if (!this.email.trim()) {
                    this.highlightCurrentField();
                    return;
                }
                this.currentStep = 2;
            } else if (step === 3) {
                if (!this.password.trim() && this.currentStep === 2) {
                    this.highlightCurrentField();
                    return;
                }
                if (!this.email.trim()) {
                    this.currentStep = 1;
                    this.highlightCurrentField();
                    return;
                }
                if (!this.password.trim()) {
                    this.currentStep = 2;
                    this.highlightCurrentField();
                    return;
                }
                this.currentStep = 3;
            }
        },
        highlightCurrentField() {
            this.isHighlighted = true;
            setTimeout(() => {
                this.isHighlighted = false;
            }, 2000); // 2 seconds highlight
        }
    }
}
</script>
<style>
@keyframes shake {
    0%, 100% { transform: translateX(0); }
    25% { transform: translateX(-8px); }
    75% { transform: translateX(8px); }
}

.animate-shake {
    animation: shake 0.5s ease-in-out;
}
</style>