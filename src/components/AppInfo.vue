<script>
export default {
    data() {
        return {
            links: [
                {
                    name: "Business",
                    icon: "fa-solid fa-chart-line"
                },
                {
                    name: "Desing",
                    icon: "fa-solid fa-palette"
                },
                {
                    name: "Development",
                    icon: "fa-solid fa-gear"
                },
                {
                    name: "Lifestyle",
                    icon: "fa-solid fa-face-smile"
                },
                {
                    name: "Office Productivity",
                    icon: "fa-solid fa-briefcase"
                }
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="my-md-container">
            <ul class="d-flex justify-content-between">
                <li v-for="link in links">
                    <i :class="link.icon"></i> <a href="">{{ link.name }}</a>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
section{
    background-color:#273044 ;
    color: white;
    ul{padding:  2rem;}
}
.my-md-container {
    width: 40%;
    margin: 0 auto;
}
</style>