<template lang="">
    <div>
        <HeaderDashboard v-model="isSidebarOpen" />
        <SideBarDashboard v-model="isSidebarOpen" />
        <DashboardContent />
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