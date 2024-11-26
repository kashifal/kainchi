<template>
    <div class="bg-[url('https://images.unsplash.com/photo-1697302548089-e3275778aff7?q=80&w=1471&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D')] mt-28 bg-cover pt-10">
        <div class="max-w-7xl  gap-x-5 gap-y-14 flex flex-wrap text-[#212121] items-start justify-between bg-white rounded-[50px] shadow-[0_0_50px_#00000014] backdrop-blur-md bg-opacity-70 p-20  my-28 mx-auto">
            <div v-for="(menu, index) in menus" class="h-fit " :key="index">
                <h1 class="md:text-[26px] sm:text-[20px] text-[18px] font-semibold">{{ menu.title }}</h1>
                <div class="mt-10 flex flex-col gap-4">
                    <a
                        v-for="(link, linkIndex) in menu.links"
                        :key="linkIndex"
                        :href="link.href"
                        class="block text-[#7A7878] sm:text-[18px]"
                    >
                        {{ link.text }}
                    </a>
                </div>
            </div>
          
        </div>
        <div class="bg-[#656565] py-4 text-center text-white sm:text-[18px]">
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
