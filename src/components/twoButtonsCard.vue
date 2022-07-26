<template>

  <div class="row align-items-center">
                <div class="col-5 ">

                    <div class="text-white">
                        <h1 class="fw-bolder">Business Planning</h1>
                        <h1 class="fw-lighter">Digital Technology</h1>
                        <h1 class="fw-bolder">Modern Solution</h1>
                    </div>

                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum, odit deserunt cum veniam
                        quaerat quisquam eos.</p>

                    <div class="ms_hero-btns">
                        <button class="ms_btn-left">Try it Now</button>
                        <button class="ms_btn-right">Explore More</button>
                    </div>
                </div>

                <div class="col-7">
                    <img src="../assets/img/header.png" alt="Hero pic">
                </div>
            </div>

</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "../styles/general.scss";
@import "../styles/variables.scss";
@import "../styles/mixins.scss";


.ms_hero {
    padding-bottom: 75px;
}

.col-5 p {
    color: $colorBg3;
    width: 60%;
    font-size: 0.7rem;
    margin: 30px 0;
}

.col-7 img {
    transform: scale(95%)
}

.ms_hero-btns button {
    @include buttonLayout;
    margin: 15px 15px 0 0;
}

button.ms_btn-left {
    background-color: $colorText9;
}

button.ms_btn-right {
    background-color: $colorBg3;
}

</style>