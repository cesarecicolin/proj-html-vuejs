<script>
import btn from "./btn.vue"
export default {
    data() {
        return {
            links: [
                {
                    img: "image_box_1-221x231.png",
                    title: "Become an instructor",
                    info: "Theach what you love. Masterstudy gives  you the tools to create a course"


                },
                {
                    img: "image_box_2-234x231.png",
                    title: "Access For Business",
                    info: "Get unlimited access to 2500 of top courses for your team"


                }
            ]
        }
    },
    methods: {

        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href
        }
    },
    components:{
        btn
    }
}
</script>
<template>
    <section class="mixin mt-5">
        <div class="card mb-3" v-for="card in links">
            <div class="row g-0 p-5">
                <div class="col-md-4">
                    <img :src=getImagePath(card.img) class="img-fluid rounded-start" alt="...">
                </div>
                <div class="col-md-8">
                    <div class="card-body ">
                        <h5 class="card-title">{{ card.title }}</h5>
                        <p class="card-text">{{ card.info }}</p>
                        <btn text="START TEACHING"/>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
.mixin{
    @include flex(row, space-evenly);
}
</style>