<template>
    <div class="relative 2xl:min-h-[80vh] min-h-screen mt-20">
        <!-- Background wrapper -->
        <div class="bg-[url('https://images.unsplash.com/photo-1697302548089-e3275778aff7?q=80&w=1471&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D')] bg-cover w-full h-[50%] absolute bottom-0 left-0"></div>
        
        <!-- Main content wrapper -->
        <div class="relative pt-28 mt-5 pb-16 h-full"> <!-- Added padding bottom for copyright bar -->
            <div class="   max-w-7xlBig mx-4 xl:mx-auto h-full">
                <div class="bg-white bg-opacity-70 relative top-2 backdrop-blur-md rounded-t-lg md:rounded-t-[50px] shadow-[0_0_50px_#00000014] 2xl:h-[80vh] h-screen p-6 md:p-10 lg:p-20">
                    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-10">
                        <div v-for="(menu, index) in menus" :key="index" class="h-fit">
                            <!-- Menu content remains the same -->
                            <h1 class="md:text-[26px] sm:text-[20px] text-[18px] font-semibold">{{ menu.title }}</h1>
                            <div class="mt-10 flex flex-col gap-4">
                                <a
                                    v-for="(link, linkIndex) in menu.links"
                                    :key="linkIndex"
                                    :href="link.href"
                                    class="block hover:underline text-[#7A7878] md:text-[18px]"
                                >
                                    {{ link.text }}
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Copyright bar -->
        <div class="bg-[#656565] w-full py-4 text-center text-white sm:text-[18px] absolute bottom-0">
            © Kain'chi - 2022. Tous droits réservés.
        </div>
    </div>
</template>

<script setup>
const menus = [
    {
        title: 'DISCOVER OUR SITE',
        links: [
            { text: 'Create new store', href: '#' },
            { text: 'FAQ', href: '#' },
        ],
    },
    {
        title: 'SUPPORT',
        links: [
            { text: 'Help center', href: '#' },
            { text: 'Guides and videos', href: '#' },
            { text: 'Product Updates', href: '#' },
            { text: 'Contact support', href: '#' },
        ],
    },
    {
        title: 'COMPANY',
        links: [
            { text: 'About', href: '#' },
            { text: 'Press and Media', href: '#' },
            { text: 'Terms of service', href: '#' },
            { text: 'Privacy Policy', href: '#' },
            { text: 'Sitemap', href: '#' },
            { text: 'Copyright policy', href: '#' },
        ],
    },
    {
        title: 'COMMUNITY',
        links: [
            { text: 'Blog', href: '#' },
            { text: 'Facebook', href: '#' },
            { text: 'Instagram', href: '#' },
            { text: 'Youtuebe', href: '#' },
        ],
    },
];
</script>
