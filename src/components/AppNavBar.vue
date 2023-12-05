<script>
import btn from "./btn.vue"
export default {
    components:{
    btn,
  }
}



</script>

<template>
    <nav class="my-container d-flex align-items-center ">


        <img src="../assets/img/MasterStudy.svg" alt="">


        <i class="fa-solid fa-bars ms-5"> CATEGORY</i>



        <input type="text" class="form-control serch ms-2" id="search" placeholder="Search coures">
        <span class="bk-blu"><i class="fa-solid fa-magnifying-glass"></i> </span>
         
        <ul class="d-flex">
            <li ><a href=""><i class="fa-solid fa-bullhorn"></i> Beacome an Instructor</a></li>
            <li class="ms-3"><a href=""><i class="fa-solid fa-briefcase"></i> For Enterprise</a></li>
        </ul>
        <ul class="d-flex align-items-center">
            <li class="ms-3"><a href=""><i class="fa-regular fa-user"></i> log in</a></li>
            <li class="ms-3"><btn/></li>
            <li class="ms-3"><i class="fa-regular fa-bookmark"></i></li>
        </ul>


    </nav>
</template>

<style lang="scss" scoped>
nav {
   

    input {
        background-color: lightgray;
        width: 500px;
    }
}

.bk-blu {
    padding: .5rem 1rem;
    border: 1px solid #457992;
    background-color: #457992;
}
</style>