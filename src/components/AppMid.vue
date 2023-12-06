<script>
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
                    type: "development",
                    img: "webDesign.jpg",
                    description: "Web Design for Begginers: Real World Coding in HTML & CSS",
                    vote: 5,
                    realPrice: 129.99,
                    discount: 65
                },
                {
                    type: "development",
                    img: "GitHub.jpg",
                    description: "GitHub Ultimate: Master Git and GitHub - Beginner to Expert ",
                    vote: 4,
                    realPrice: 99.99,
                    discount: 50
                },
                {
                    type: "development",
                    img: "ios11.jpg",
                    description: "The complete IOS 11 & Swift  Developer Course - Build 20 Apps",
                    vote: 4,
                    realPrice: 199.99,
                    discount: 100
                },
                {
                    type: "development",
                    img: "java.jpg",
                    description: "Android Java Masterclass-Become an App Developer",
                    vote: 5,
                    realPrice: 99.99,
                    discount: 50
                },
                {
                    type: "development",
                    img: "xamarin.jpg",
                    description: "Xamarin Forms Build Native Cross-platform Apps whith C#",
                    vote: 4,
                    realPrice: 189.99,
                    discount: 95
                },
            ]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href
        }
    }
}
</script>
<template>
    <h3 class="mt-5 ms-5">Popular Development Courses</h3>
    <div class="row ms-5 mt-5">
        <div class="card  my-card" v-for="card in courses ">
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
