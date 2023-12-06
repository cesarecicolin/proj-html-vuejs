<script>
import btn from "./btn.vue"
export default {
    data() {
        return {
            courses: [
                {
                    type: "development",
                    img: "Swift3.jpg",
                    description: "The complete IOS 10 & Swift 3 Developer Course",
                    vote: 4,
                    realPrice: 199.99,
                    discount: 100
                },
                {
                    type:"design",
                    img:"css.jpg",
                    description:"CSS-The Complete Guide 2020(incl,Flexbox,grid & SASS)",
                    vote: 5,
                    realPrice:199.99,
                    discount:100

                },
                {
                    type: "development",
                    img: "webDesign.jpg",
                    description: "Web Design for Begginers: Real World Coding in HTML & CSS",
                    vote: 5,
                    realPrice: 129.99,
                    discount: 65
                },
                {
                    type: "Design",
                    img: "digitalpaint.jpg",
                    description: "Digitally Painting Light and Color: Amateur to Master",
                    vote: 4,
                    realPrice: 139.99,
                    discount: 70
                },
                {
                    type: "Arts & Crafts",
                    img: "arabic.jpg",
                    description: "Become an Arabic Calligraphy Artist from Scratch",
                    vote: 5,
                    realPrice: 199.99,
                    
                },
                {
                    type: "Google",
                    img: "ninja.jpg",
                    description: "Google searching Ninja!",
                    vote: 4,
                    realPrice: 89.99,
                    discount: 45
                },
                {
                    type: "Art & Crafts",
                    img: "whatercolor.jpg",
                    description: "Foundations for Mastering Wathercolor Painting",
                    vote: 5,
                    realPrice: 19.99,
                    discount: 10
                },
                {
                    type: "Food & Beverage",
                    img: "wine.jpg",
                    description: "Get Wine-Smart",
                    vote: 4,
                    realPrice: 49.99,
                    discount: 25
                },
                {
                    type: "Art & Crafts",
                    img: "pencil.jpg",
                    description: "The colored Pencil Drawing Course",
                    vote: 4,
                    realPrice: 34.99,
                    discount: 18
                },
                {
                    type: "Art & Crafts",
                    img: "realistic.jpg",
                    description: "Paint Realistic Watercolor and Botanicals-STUDIO BASICS",
                    vote: 5,
                    realPrice: 69.99,
                    discount: 35
                },
                {
                    type: "Art & Crafts",
                    img: "brushstokes.jpg",
                    description: "Mastering Brushstrokes -part 1",
                    vote: 5,
                    realPrice: 19.99,
                    discount: 10
                },
                {
                    type: "Art & Crafts",
                    img: "magnolias.jpg",
                    description: "Paint Realistic Watercolour and Botanicals - MAGNOLIAS",
                    vote: 5,
                    realPrice: 69.99,
                    discount: 35
                },
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
    
    <div class="row ms-5 mt-5">
        <div class="card  my-card ms-2 mt-5" v-for="card in courses ">
            <img :src="getImagePath(card.img)" class="card-img-top" alt="">
            <div class="card-body">
                <h5 class="card-title">{{ card.type }} ></h5>
                <p class="card-text">{{ card.description }}
                </p>
                <hr>
                <div class=" mixin">    
    
                    <span>{{ card.vote }}</span>
                    <div class="mini-mixin">
                        <span class="sconto">{{ card.realPrice }}</span>
                        <span>{{ card.discount }}</span>
                    </div>

                </div>
            </div>
        </div>
    </div>
    <div class="d-flex justify-content-center mt-5">
         <btn class="text-center d-block"/>
    </div>
   
</template>
<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
img {
    width: 100%;
}
.mixin{
    @include flex(row, space-between);
       div{
        @include flex(column, );
        .sconto{
            text-decoration: line-through;
            color: rgba($color: #000000, $alpha: .5);
        }
       }
         
}

.my-card {
    width: calc(80% / 5);

}

</style>