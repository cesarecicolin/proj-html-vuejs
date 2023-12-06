<script>
</script>
<template>
    <section class="mt-5">
        <div class="mixin">
            <div>
                <h2>Subscribe our newsletter</h2>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam odio amet praesentium quia accusantium
                    corrupti possimus, rem deserunt explicabo neque eos? </p>
            </div>
            <div class="d-flex align-items-end">
                <div>
                    <label for="exampleInputEmail1" class="form-label">YOUR EMAIL ADRESS</label>
                <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Enter your email">
                </div>
                <div>
                    <button>SUBSCRIBE</button>
                </div>
                
            </div>
        </div>

    </section>
</template>
<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
section{
    background-color: #ff4450;
    .mixin {
    width: 60%;
    margin: 0 auto;
    @include flex(row, space-between);
    padding: 1rem 0;
    color: white;
    input{
        width: 300px;
        border-radius: 0;
        padding: .5rem 1rem;
    }
    button{
        padding: .5rem 1rem;
        background-color: #457992;
        border: none;
    }
}
}

</style>