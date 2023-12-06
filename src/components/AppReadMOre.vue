<script>
import btn from "./btn.vue"
export default {
    components:{
        btn
    }
    
}

</script>
<template>
<section class="mt-5">
    <div>
        <h2>LimiTless learnig, more possibilities</h2>
        <p>Online courses open the opportunity for learnig to almost anyone regarldless of their scheduling commitens.</p>
        <btn text="READ MORE"/>
    </div>
</section>
</template>
 
<style lang="scss" scoped>
section{background-image: url(../assets/img/bg.png);


background-repeat: no-repeat;
background-size: cover;

div{
    *{margin-bottom: 1rem;}
    width: 50%;
    padding-top: 15rem;
    padding-left: 20rem;
    h2{font-size: 3rem;
    }
    p{font-size: 1.5rem;}
    padding-bottom: 10rem;
}
}
</style>