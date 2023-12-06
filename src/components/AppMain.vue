<script>
import AppCourses from './AppCourses.vue';
import AppMid from './AppMid.vue';
import AppReadMOre from "./AppReadMOre.vue"
import RecentCourses from './RecentCourses.vue';

export default {
    components:{
    AppMid,
    AppReadMOre,
    RecentCourses,
    AppCourses
}
}
</script>
<template>
    <AppMid/>
    <AppReadMOre/>
    <RecentCourses/>
    <AppCourses/>
</template>
<style lang="scss" scoped>

</style>