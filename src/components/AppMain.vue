<script>
import AppCourses from './AppCourses.vue';
import AppMid from './AppMid.vue';
import AppReadMOre from "./AppReadMOre.vue"
import RecentCourses from './RecentCourses.vue';
import NewsLetter from "./NewsLetter.vue"
import PopularCors from "./PopularCors.vue"

export default {
    components:{
    AppMid,
    AppReadMOre,
    RecentCourses,
    AppCourses,
    NewsLetter,
    PopularCors

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
</template>
<style lang="scss" scoped>

</style>