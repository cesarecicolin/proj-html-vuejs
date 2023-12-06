<script>
import AppParteSuperiore from "./components/AppParteSuperiore.vue"
import AppHero from "./components/AppHero.vue"
import AppMain from "./components/AppMain.vue"
export default {
  components:{
    AppParteSuperiore,
    AppHero,
    AppMain
  }
 
  
}
</script>

<template>
 <AppParteSuperiore/>
 <AppHero/>
 <AppMain/>
 
</template>

<style lang="scss">
@use "./style/general.scss";
@import "@fortawesome/fontawesome-free/css/all.css";
</style>
