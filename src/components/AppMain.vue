<script>
import AppCourses from './AppCourses.vue';
import AppMid from './AppMid.vue';
import AppReadMOre from "./AppReadMOre.vue"
import RecentCourses from './RecentCourses.vue';
import NewsLetter from "./NewsLetter.vue"
import PopularCors from "./PopularCors.vue"
import InstructorBusiness from './InstructorBusiness.vue';

export default {
    components:{
    AppMid,
    AppReadMOre,
    RecentCourses,
    AppCourses,
    NewsLetter,
    PopularCors,
    InstructorBusiness
}
}
</script>
<template>
    <AppMid/>
    <AppReadMOre/>
    <RecentCourses/>
    <AppCourses/>
    <NewsLetter/>
    <PopularCors/>
    <InstructorBusiness/>
</template>
<style lang="scss" scoped>

</style>