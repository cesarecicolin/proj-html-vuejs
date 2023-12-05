<script>
export default {
    data() {
        return {
            links: ["Home", "Pages", "Course Formats", "Courses", "Demos"]
        }
    }
}
</script>

<template>
    <div class="my-container d-flex justify-content-between">
        <div >
            <select class="form-select">
                <option selected>English</option>
                <option value="1">Italiano</option>
            </select>
        </div>
        <div>
            <ul class="d-flex ">
                <li class="ms-4" v-for="link in links">
                    <a href="">{{ link }}</a>
                </li>
                <li class="ms-4"><a href=""><i class="fa-brands fa-facebook"></i></a></li>
                <li class="ms-4"><a href=""><i class="fa-brands fa-twitter"></i></a></li>
                <li class="ms-4"><a href=""><i class="fa-brands fa-instagram"></i></a></li>
                <li class="ms-4"><a href=""><i class="fa-brands fa-linkedin"></i></a></li>
                <li class="ms-4"><a href=""><i class="fa-brands fa-google-plus-g"></i></a></li>
                <li class="ms-4"><a href=""><i class="fa-brands fa-youtube"></i></a></li>               
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
select {
    border: none;
    width: 100px;
    color: #aaaaaa;
}
.container{
    color:#aaaaaa ;
}

</style>