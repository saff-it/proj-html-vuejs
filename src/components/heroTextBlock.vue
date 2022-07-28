<template>
    <div class="col-5 ">

        <div class="text-white">
            <span>{{textItem.pretitle}}</span>
            <h1 class="fw-bolder mt-4">{{textItem.h1A}}</h1>
            <h1 class="fw-lighter">{{textItem.h1B}}</h1>
            <h1 class="fw-bolder">{{textItem.h1C}}</h1>
        </div>

        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum, odit deserunt cum veniam
            quaerat quisquam eos.</p>

        <div class="ms_hero-btns">
            <button class="ms_btn-left">Try it Now</button>
            <button class="ms_btn-right">Explore More</button>
        </div>
    </div>
</template>

<script>
export default {
    props: ['textItem']
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
    @include gradientRed;

}

button.ms_btn-right {
    @include gradientBlue;

}

</style>