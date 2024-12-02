<template lang="">
    <div>
        <div class="absolute bg-[#6E3191] z-[2] bg-opacity-20 blur-[80px] rounded-full size-60 top-0 left-0"></div>
        <div class="absolute bg-[#6E3191] z-[2] bg-opacity-30 blur-[200px] rounded-full size-[300px] sm:size-[400px] md:size-[500px] top-0 right-0"></div>
       <div class="relative">
        <HeaderDashboard v-model="isSidebarOpen" />
        <SideBarDashboard v-model="isSidebarOpen" />
        <DashboardContent />
        <DashboardFooter />
       </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            isSidebarOpen: false
        }
    }
}
</script>
<style lang="">
    
</style>