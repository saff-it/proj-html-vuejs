<template>
    <main>

        <!-- what we do section  -->
        <section>
            <div class="container">

                <div class="ms_upper-txt">
                    <span>Our Services</span>
                    <h2> <span class="ms_bolder-txt">What</span> We Do </h2>
                    <span>When, while the lovely valley teems with vapour around meand the</span>
                </div>

                <div class="row">
                    <whatWeDoCard v-for="(card, index) in whatWeDoCards" :key="index" :singleCard="card" />
                </div>

                <button>View All Services</button>

            </div>
        </section>

        <!-- grow your business section  -->
        <section class="ms_grow-business">
            <div class="container ms_hero">
                <div class="row align-items-center">

                    <div class="col-7">
                        <img src="../assets/img/men-data.png" alt="Hero pic">
                    </div>

                    <div class="col-5">

                        <div class="ms_title-txt text-white">
                            <span>Start your Project</span>
                            <h1 class="fw-bolder mt-3">Grow your Business</h1>
                            <h1 class="fw-lighter">With our Strategy</h1>
                        </div>

                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum, odit deserunt cum veniam
                            quaerat quisquam eos.</p>

                        <div class="ms_hero-btns">
                            <button class="ms_btn-left">Try it Now</button>
                            <button class="ms_btn-right">Explore More</button>
                        </div>
                    </div>
                   
                </div>
            </div>
        </section>

    </main>
</template>

<script>
import whatWeDoCard from './whatWeDoCard.vue'

export default {
    name: 'siteMain',
    components: {
        whatWeDoCard,

    },

    data: function () {
        return {

            whatWeDoCards: [

                {
                    title: 'Data Analysis',
                    pic: '../assets/img/Group-247.png',
                },
                {
                    title: 'SEO Optimization',
                    pic: '../assets/img/Group-567.png',
                },
                {
                    title: 'Security Data',
                    pic: '../assets/img/Group-538.png',
                },
                {
                    title: 'Branding Strategy',
                    pic: '../assets/img/Group-566.png',
                },

            ],
        }
    },



}
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";
@import "../styles/variables.scss";
@import "../styles/mixins.scss";

div.container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

// WHAT WE DO SECTION

.ms_upper-txt {
    text-align: center;
    margin: 70px;

    span:first-child {
        color: $colorText9;
    }

    h2 {
        font-size: 3rem;
        margin: 10px;
        font-weight: 400;

        span.ms_bolder-txt {
            font-weight: 900;
            color: black;
        }
    }
}

button {
    @include buttonLayout;
    background-color: $colorText9;
    width: 12%;
    margin-top: 150px;
    margin-bottom: 90px;
}

// GROW YOUR BUSINESS SECTION

section.ms_grow-business{
    background-color: $colorBg9;
}

.col-5 div.ms_title-txt span{
    font-size: 0.8rem;
}

.col-5 p {
    color: $colorBg3;
    width: 60%;
    font-size: 0.7rem;
    margin: 30px 0;
}

.col-7 img {
    transform: scale(60%)
}

.ms_hero-btns button {
    @include buttonLayout;
    margin: 15px 15px 0 0;
    width: 30%;
}

button.ms_btn-left {
    background-color: $colorText9;
}

button.ms_btn-right {
    background-color: $colorBg3;
}

</style>