<template>

    <header>

        <!-- top header  -->
        <nav class="container ms_top-header">

            <div class="ms_logo-container">
                <img src="../assets/img/white-logo-2.png" alt="Logo">
            </div>

            <div class="ms_nav-list">

                <ul>
                    <li v-for="(link, index) in headerNavLinks" :key="index"> {{ link.text }}</li>

                </ul>

                <button>
                    Sign In
                </button>

            </div>
        </nav>

        <!-- bottom header/hero  -->
        <div class="container ms_hero">
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

        </div>

    </header>

</template>

<script>

export default {

    name: 'siteHeader',
    components: {

    },

    data: function () {
        return {

            headerNavLinks: [
                {
                    text: 'Home',
                    url: '#',
                }, {
                    text: 'About',
                    url: '#',
                }, {
                    text: 'Services',
                    url: '#',
                }, {
                    text: 'Blog',
                    url: '#',
                }, {
                    text: 'Contact',
                    url: '#',
                }, {
                    text: 'Portfolio',
                    url: '#',
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


// TOP HEADER 

header {
    background-color: $colorBg9;
}

nav.ms_top-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.ms_logo-container img {
    width: 75%;
    padding: 15px 0;
}

.ms_nav-list {
    display: flex;
    align-items: center;

    ul {
        list-style: none;
        margin: 0 30px;

        li {
            display: inline-block;
            margin: 0 10px;
            color: white;
            font-size: 0.9rem;
        }
    }

    button {
        @include buttonLayout;
        @include gradientBlue;

    }
}

// HERO 

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