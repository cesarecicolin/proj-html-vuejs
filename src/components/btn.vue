<script>

export default {
   props:{
    text: String,
   }
}
</script>

<template>
    <button>{{ text }}</button>
</template>
 
<style lang="scss" scoped>
button{
    padding: 1rem 2rem;
    border: 1px solid red;
    border-radius: 25px;
    background-color: red;
    color: white;
}
</style>