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
                    type: "design",
                    img: "css.jpg",
                    description: "CSS-The Complete Guide 2020(incl,Flexbox,grid & SASS)",
                    vote: 5,
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






            ]
        }
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href
        }
    },

}
</script>
<template>
    <section>
        <div class="text-center ">
            <h2 class="pt-4">Popular Courses</h2>
            <p>Discover our most popular courses for self learnig</p>
        </div>
        <div>
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
        </div>
        <div class="d-flex justify-content-center mt-5">
            <button>&LeftArrow;</button><button>&rightarrow;</button>
        </div>
        
    </section>
</template>
<style lang="scss" scoped>
@use "../style/partials/mixin" as *;

section{background-color: lightgray;}
img {
    width: 100%;
}

.mixin {
    @include flex(row, space-between);

    div {
        @include flex(column, );

        .sconto {
            text-decoration: line-through;
            color: rgba($color: #000000, $alpha: .5);
        }
    }

}

.my-card {
    width: calc(80% / 5);

}
button{padding: .5rem 1rem;
background-color: white;
border-color: lightgray;
color: rgba($color: #000000, $alpha: .5);
margin-bottom: 1rem;
}

</style>