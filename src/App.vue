<script>
import AppParteSuperiore from "./components/AppParteSuperiore.vue"
import AppHero from "./components/AppHero.vue"
import AppMid from "./components/AppMid.vue"
export default {
  components:{
    AppParteSuperiore,
    AppHero,
    AppMid
  }
 
  
}
</script>

<template>
 <AppParteSuperiore/>
 <AppHero/>
 <AppMid/>
</template>

<style lang="scss">
@use "./style/general.scss";
@import "@fortawesome/fontawesome-free/css/all.css";
</style>
