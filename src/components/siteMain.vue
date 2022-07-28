<template>
    <main>

        <!-- what we do section  -->
        <section>
            <div class="container ms_we-do-container">

                <blockItems v-for="(item, index) in wwdBlockItems" :key="index"
                            :singleItem="item"
                />

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

        <!-- pricing section  -->
        <section class="ms_pricing-bg">

            <div class="container">

                <blockItems v-for="(item, index) in priceBlockItems" :key="index"
                            :singleItem="item"        
                />

            </div>

            <div class="container ms_pricing-cards-cont">
                <div class="row">
                    <div class="col-4 w-100 d-flex">
                        <PricingCard v-for="(card, index) in pricingCards" :key="index" :class="addSpecialClass(index)"
                            :singlePricingCard="card" />

                    </div>
                </div>
            </div>

        </section>

        <!-- latest posts section  -->
        <section class="ms_posts-section">

            <div class="container ms_posts-text">
                <blockItems v-for="(item, index) in postsBlockItems" :key="index"
                            :singleItem="item"
                />
            </div>


            <div class="container ms_posts-box pb-5">
                <div class="row">
                    <postCard v-for="(card, index) in postCards" :key="index" :singlePostCard="card"
                        :class="addSpecialClassToPost(index)" />
                </div>
            </div>


        </section>

        <!-- testimonial section  -->
        <section class="ms_testimonial-section">

            <!-- section's text  -->
            <div class="container ms_posts-text">

                <blockItems v-for="(item, index) in testimonialBlockItems" :key="index"
                            :singleItem="item"
                />

            </div>

            <!-- section's cards  -->
            <div class="container pt-5">
                <div class="row">
                    <testimonialCard v-for="(card, index) in testimonialCards" :key="index" :testimonialCard="card" />
                </div>
            </div>

            <!-- section's logos  -->
            <div class="container ms_partners-logo">
                <partnersLogoCard v-for="(logo, index) in partnersLogos" :key="index" :singleLogo="logo" />
            </div>

            <!-- section's subrscire bar  -->
            <div class="container ms_subscribe-bar">
                <div class="ms_bar-txt">
                    <h2>We Offer Awesome Services</h2>
                    <p>When, while the lovely valley teems with vapour
                        around meanthe while the lovely valley teems</p>
                </div>

                <div class="ms_bar-input">
                    <input type="text" placeholder="Enter your Email Address">
                    <button>Subscribe</button>
                </div>

            </div>


        </section>


    </main>
</template>

<script>
import whatWeDoCard from './whatWeDoCard.vue'
import carouselCard from './carouselCard.vue'
import PricingCard from './pricingCard.vue'
import postCard from './postCard.vue'
import testimonialCard from './testimonialCard.vue'
import partnersLogoCard from './partnersLogoCard.vue'
import blockItems from './blockItems.vue'

export default {
    name: 'siteMain',
    components: {
        whatWeDoCard,
        carouselCard,
        PricingCard,
        postCard,
        testimonialCard,
        partnersLogoCard,
        blockItems,
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

            wwdBlockItems: [

                {
                    pretitle: 'Our Services',
                    titleBold: 'What',
                    titleLight: 'We Do',
                    subtitle: "When, while the lovely valley teems with vapour around meand the",
                    special: false,
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

            pricingCards: [

                {
                    title: 'Designing',
                    subTitle: "process",
                    price: "40",
                },
                {
                    title: 'Developing',
                    subTitle: "product",
                    price: "60",
                },
                {
                    title: 'Supporting',
                    subTitle: "clients",
                    price: "80",
                },
            ],

            priceBlockItems: [

                {
                    pretitle: 'Price List',
                    titleBold: 'Our',
                    titleLight: 'Pricing',
                    subtitle: "When, while the lovely valley teems with vapour around meand the",
                    special: true,
                },

            ],

            postCards: [

                {
                    title: 'Amazon gets CCI not to acquire 49% stake in',
                    paragraph: "When, while with le the lovely valley teems with vapouaround meand the",
                },
                {
                    title: 'Clearing Corporations get SEBI nod to invest in overnight funds',
                    paragraph: "When, while with le the lovely valley teems with vapouaround meand the",
                },
                {
                    title: 'Shabnam Dhillion, wife of RSSb chief Gurinder Dhollon, passes away London',
                    paragraph: "When, while with le the lovely valley teems with vapouaround meand the",
                },

            ],

            postsBlockItems: [

                {
                    pretitle: 'Blog',
                    titleBold: 'Latest',
                    titleLight: 'Posts',
                    subtitle: "When, while the lovely valley teems with vapour around meand the while the lovely valley teems with vapou",
                    special: false,
                },

            ],

            testimonialCards: [

                {
                    img: 'szabo-viktor-1266895-unsplash-1024x1024.png',
                    name: "Michkel Angel",
                    job: "Marketing Manager",
                },
                {
                    img: 'philipe-cavalcante-539505-unsplash-1024x1024.png',
                    name: "Maria Dolores",
                    job: "Projecy Manager",
                },
                {
                    img: 'fabio-spinelli-695744-unsplash-1024x1024.png',
                    name: "Paola Perego",
                    job: "SEO Specialist",
                },

            ],

            testimonialBlockItems: [

                {
                    pretitle: 'Testimonial',
                    titleBold: 'What',
                    titleLight: 'People Say',
                    subtitle: "When, while the lovely valley teems with vapour around meand the while the lovely valley teems with vapou",
                    special: false,

                },

            ],

            partnersLogos: [

                {
                    img: 'client-1-1.png',
                },
                {
                    img: 'clienty-2.png',
                },
                {
                    img: 'clienty-3.png',
                },
                {
                    img: 'clienty-4.png',
                },
                {
                    img: 'client-5.png',
                },

            ],
        }
    },

    methods: {
        addSpecialClass(indexActive) {
            let cssClass = '';

            if (indexActive === 1) {
                cssClass = 'special';
            }

            return cssClass;
        },

        addSpecialClassToPost(indexActive) {
            let cssPostClass = '';

            if (indexActive === 0) {
                cssPostClass = 'col-6 ms_post-cards-wide';
            } else {
                cssPostClass = 'col-3 ms_post-cards';
            }

            return cssPostClass;
        }

    }

}
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";
@import "../styles/variables.scss";
@import "../styles/mixins.scss";

.container.ms_we-do-container {
    display: flex;
    align-items: center;
    flex-direction: column;

}

// WHAT WE DO SECTION

button.ms-wwd-btn {
    @include buttonLayout;
    @include gradientRed;
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
    @include gradientRed;
}

button.ms_btn-right {
    @include gradientBlue;
}


// CAROUSEL SECTION 

section.ms_carousel-bg {
    background-color: $colorText3;
}

.ms_carousel-bar {
    width: 100%;
    padding: 110px 0 0 0;
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
    padding: 50px 0 40px 0;
    color: $colorBg2;
    text-align: center;

    i {
        padding: 3px;
        font-size: 0.5rem;
    }
}

.ms_carousel-slider i:first-child {
    color: $colorText9;
}


// PRICING SECTION 

.ms_pricing-bg {
    background-color: $colorBg9;
    position: relative;
    height: 500px;

}

.ms_pricing-cards-cont {
    position: absolute;
    top: 260px;
    left: 265px;

}

.ms_pricing-txt {
    @include displayFlexToColumn;
    color: white;
    padding: 60px 0;


    span:first-child {
        color: $colorText9;
    }

    .ms_pricing-span-sizing {
        font-size: 0.8rem;
        width: 80%;
        text-align: center;

    }

    h2 {
        font-size: 3rem;
        margin: 10px;
        font-weight: 400;

        span.ms_bolder-txt {
            font-weight: 900;
            color: white;
        }
    }
}

// POSTS SECTION 

.ms_posts-section {
    background-color: $colorText3;


    .ms_posts-text {
        padding-top: 350px;
        padding-bottom: 30px;
    }
}

// COMPANY LOGOS SECTIOM 

.ms_partners-logo{
    padding-bottom: 120px;
}

// TESTIMONIAL SECTION 

.ms_testimonial-section {
    background-color: $colorText3;
    position: relative;

}

.ms_subscribe-bar {
    @include displayFlex;
    @include gradientRed;
    padding: 55px 30px;
    border-radius: 20px;
    position: absolute;
    bottom: -85px;
    left: 180px;


    .ms_bar-txt {
        color: white;

        p {
            margin: 0;
            font-size: 0.8rem;
            font-weight: lighter;
        }
    }

    .ms_bar-input{
        @include displayFlex;
        background-color: white;
        height: 40px;
        width: 30%;
        border-radius: 20px;

        input{
            border: none;
            font-size: 0.8rem;
            margin-left: 20px;

            &::placeholder{
                color: $colorText6;

            }
        }

        button{
           @include buttonLayout;
           background-color: $colorText8; 
           margin-right: 3px;

        }
    }



}
</style>