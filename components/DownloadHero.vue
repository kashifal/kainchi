<template lang="">
    <div class="py-20 max-w-5xl mx-auto px-4">
        <h1 class="lg:text-[74px] md:text-[40px] text-[30px] leading-none text-center text-[#3A0CA3] font-bold">
            DOWNLOAD<br />Apple Apps
        </h1>
        <p class="text-[#212121] text-sm py-3 text-center">
            By installing our apps, you agree to our Terms & Privacy Policy.
        </p>
        <div class="grid md:grid-cols-2 min-h-[568px] gap-14 my-10">
            <div 
                v-for="(card, index) in cards" 
                :key="index" 
                class="relative min-h-[458px] md:min-h-auto group cursor-pointer bg-[#3A0CA3] text-white text-center rounded-[20px] flex flex-col items-center justify-between gap-8 px-4 py-12"
            >
                <div class="flex flex-col relative z-[4] gap-6">
                    <h5 class="lg:text-[18px]">{{ card.device }}</h5>
                    <h1 class="lg:text-[74px] md:text-[40px] text-[30px]">{{ card.platform }}</h1>
                    <p class="">{{ card.description }}</p>
                </div>
                <div class="bg-[#212121] absolute group-hover:bottom-5 group-hover:w-[90%] group-hover:left-[5%] w-full h-full bottom-0 left-0 z-[2] group-hover:h-20 transition-all duration-1000 flex rounded-2xl items-center justify-center">
                </div>
                <img class="relative z-[4] w-40 top-5" :src="card.image" :alt="card.alt" />
            </div>
        </div>
        <p class="sm:text-[18px] text-[#212121] mt-10 text-center">Visit kainchi.com/dl on your mobile phone to install</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            // Array of card data
            cards: [
                {
                    device: "Mobile and Tablet",
                    platform: "Android",
                    description: "Experience the best apps on your Apple devices.",
                    image: "https://scontent.xx.fbcdn.net/v/t1.15752-9/462546579_589354170152482_6098471366466255736_n.png?_nc_cat=111&ccb=1-7&_nc_sid=0024fc&_nc_ohc=yEUlW0mVWxgQ7kNvgFM_-JE&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent.xx&oh=03_Q7cD1QE3gJ1HmJLPV6Zf8h3OhvcXZtRMzOHNsrP772moe51quA&oe=676D1BE4", // Replace with actual path
                    alt: "Apple Store"
                },
                {
                    device: "Mobile and Tablet",
                    platform: "Mac",
                    description: "Powerful tools optimized for your Mac.",
                    image: "https://scontent.xx.fbcdn.net/v/t1.15752-9/462541286_1108872293943612_323255001297040986_n.png?_nc_cat=104&ccb=1-7&_nc_sid=0024fc&_nc_ohc=CEEJBJd21VIQ7kNvgFjx1Pt&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent.xx&oh=03_Q7cD1QGstVuAuSP1dGjZgYAkKp-Wdydxn8L2YyDdn05rO0K6vA&oe=676D143A", // Replace with actual path
                    alt: "Mac App Store"
                }
            ]
        };
    }
};
</script>

<style lang="">
/* Add any additional styles if needed */
</style>
