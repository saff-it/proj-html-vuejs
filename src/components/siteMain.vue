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
                    <whatWeDoCard v-for="(card, index) in whatWeDoCards" :key="index"
                    :singleCard="card" />
                </div>

                <button>View All Services</button>

            </div>
        </section>

        <!-- grow your business section  -->

        <section></section>




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
</style>