<script>
export default {
    data(){
        return{
            categories:
            [
                "All Categories", "BUsiness", "Design", "Development" , "IT & Software",
                "LifeStyle", "Marketing", "Office Productivity"
            ]
        }
    }
}
</script>

<template>
    <section>
        <div>
            <h2 class="text-center">Recent courses</h2>
            <ul class="mixin ">
                <li v-for="categorie in categories">
                {{ categorie }}
                </li>
            </ul>
        </div>
    </section>

</template>
<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
.mixin{
    @include flex(row, );
    margin-top: 2rem;
    text-align: center;
    li{
        margin-left: 2rem;
    }
}
</style>