<template>

    <div>

        <div class="ms_post-card">
            <div class="mt-3 ms_txt-post">
                <span>April 21, 2019 - Paul</span>
                <h6>Clearing Corporations get SEBI nod to invest in overnight funds</h6>
                <p>When, while with le the lovely valley teems with vapouaround meand the</p>
            </div>

            <div>
                <button>Read More</button>
            </div>

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


.ms_post-cards {
    display: flex;

    .ms_post-card {
        display: flex;
        flex-direction: column;
        align-items: left;
        background-color: $colorBg9;
        color: white;
        padding: 25px 40px;
        margin: 0 5px;
        border-radius: 20px;

        span {
            font-size: 0.7rem;
            font-weight: lighter;
        }

        h6 {
            margin: 20px 0;
        }

        p {
            width: 90%;
            text-align: left;
            font-size: 0.7rem;
            margin: 0;

        }

        button {
            @include buttonLayout;
            color: black;
            width: 70%;
            margin-top: 40px;
        }
    }

}

.ms_post-cards-wide {
    display: flex;
    

    .ms_post-card {
        display: flex;
        align-items: flex-end;
        justify-content: space-between;
        background-image: url('../assets/img/headway-537308-unsplash-1380x703.jpg');
        background-size: cover;
        color: white;
        padding: 25px 40px;
        margin: 0 5px;
        border-radius: 20px;

        span {
            font-size: 0.7rem;
            font-weight: lighter;
            margin-top: 20px;
        }

        h6 {
            margin: 20px 0;
        }

        p {
            width: 90%;
            text-align: left;
            font-size: 0.7rem;
            margin: 0;
        }

        button {
            @include buttonLayout;
            color: black;
            width: 100%;
            margin-top: 40px;

        }
    }

    .ms_txt-post{
        width: 65%;
    }

}
</style>