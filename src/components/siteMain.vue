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
                    <whatWeDoCard v-for="(card, index) in whatWeDoCards" :key="index" :singleCardWeDo="card" />
                </div>

                <button class="ms-wwd-btn">View All Services</button>

            </div>
        </section>

        <!-- grow your business section  -->
        <section class="ms_grow-business">
            <div class="container ms_hero">
                <div class="row align-items-center">

                    <div class="col-7 ms_grow-img">
                        <img src="../assets/img/men-data.png" alt="Hero pic">
                    </div>

                    <div class="col-5 ms_grow-txt">

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

        <!-- latest work carousel  -->
        <section class="ms_carousel-bg">
            <div class="container">

                <div class="ms_carousel-bar">

                    <div class="ms_carousel-bar-txt">
                        <span>Portfolio</span>
                        <h2> <span class="ms_bolder-txt">latest</span> work </h2>

                    </div>

                    <div class="ms_carousel-bar-btns align-self-end">

                        <div class="ms_caro-btn-lft me-4">
                            <i class="fa-solid fa-arrow-left"></i>
                        </div>

                        <div class="ms_caro-btn-rgt">
                            <i class="fa-solid fa-arrow-right"></i>
                        </div>

                    </div>

                </div>


                <div class="row ms_carousel-cards">
                    <carouselCard v-for="(card, index) in carouselCards" :key="index" :singleCarouselCard="card" />

                </div>

                <div class="ms_carousel-slider">
                    <i class="fa-solid fa-circle"></i>
                    <i class="fa-solid fa-circle"></i>
                    <i class="fa-solid fa-circle"></i>
                    <i class="fa-solid fa-circle"></i>
                    <i class="fa-solid fa-circle"></i>
                </div>


            </div>

        </section>

    </main>
</template>

<script>
import whatWeDoCard from './whatWeDoCard.vue'
import carouselCard from './carouselCard.vue'

export default {
    name: 'siteMain',
    components: {
        whatWeDoCard,
        carouselCard,

    },

    data: function () {
        return {

            whatWeDoCards: [

                {
                    title: 'Data Analysis',
                    pic: "Group-247.png",
                },
                {
                    title: 'SEO Optimization',
                    pic: 'Group-567.png',
                },
                {
                    title: 'Security Data',
                    pic: 'Group-538.png',
                },
                {
                    title: 'Branding Strategy',
                    pic: 'Group-566.png',
                },

            ],

            carouselCards: [

                {
                    img: '8wa60okr-1-790x576.jpg',
                    title: "Basket of Flower on table",
                    type: "Branding Strategy",
                },
                {
                    img: 'DRY-1-790x576.jpg',
                    title: "Purinky Products",
                    type: "Digital Experience",
                },
                {
                    img: 'a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg',
                    title: "Satisfy Poster",
                    type: "Branding Strategy",
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

button.ms-wwd-btn {
    @include buttonLayout;
    background-color: $colorText9;
    width: 12%;
    margin-top: 150px;
    margin-bottom: 90px;
}

// GROW YOUR BUSINESS SECTION

section.ms_grow-business {
    background-color: $colorBg9;
}

div.ms_title-txt span {
    font-size: 0.8rem;
}

.ms_grow-txt p {
    color: $colorBg3;
    width: 60%;
    font-size: 0.7rem;
    margin: 30px 0;
}

.ms_grow-img img {
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


// CAROUSEL SECTION 

section.ms_carousel-bg {
    background-color: $colorText3;
}

.ms_carousel-bar {
    width: 100%;
    margin: 110px 0 40px 0;
    @include displayFlex;


    span:first-child {
        color: $colorText9;
    }

    h2 {
        font-size: 3rem;
        font-weight: 400;

        span.ms_bolder-txt {
            font-weight: 900;
            color: black;
        }
    }
}

.ms_carousel-bar-btns {
    @include displayFlex;

    .ms_caro-btn-lft,
    .ms_caro-btn-rgt {
        font-size: 0.9rem;
        border: 1px solid $colorText9;
        color: $colorText9;
        padding: 10px 14px;
        border-radius: 50%;

    }

}


.ms_carousel-slider {
    margin: 50px 0 40px 0;
    color: $colorBg2;

    i {
        padding: 3px;
        font-size: 0.5rem;
    }
}

.ms_carousel-slider i:first-child{
    color: $colorText9;
}
</style>