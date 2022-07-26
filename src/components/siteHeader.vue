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
            <twoButtonsCard />

        </div>

    </header>
</template>

<script>
import twoButtonsCard from './twoButtonsCard.vue'


export default {

    name: 'siteHeader',
    components: {
        twoButtonsCard,

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

<style lang="scss">
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
        background-color: $colorBg3;
    }
}



</style>