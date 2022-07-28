<template>
    <div class="col-4 p-0 ms_carousel-card">

        <div class="ms_card-img">
            <img class="w-100" :src="require(`../assets/img/${singleCarouselCard.img}`)" :alt="singleCarouselCard.title">
        </div>

        <div class="ms_card-txt">
            <span class="ms_card-txt-sx">{{singleCarouselCard.title}}</span>
            <span class="ms_card-txt-dx">{{singleCarouselCard.type}}</span>
        </div>

    </div>
</template>



<script>
export default {
    props: ['singleCarouselCard'],
}
</script>



<style lang="scss">
@import "../styles/general.scss";
@import "../styles/variables.scss";
@import "../styles/mixins.scss";

.ms_carousel-card:hover{
    @include gradientRed;
    cursor: pointer;
    color: white;
}

.ms_card-img img{
    border-radius: 20px;
}

.ms_card-txt{
    display: flex;
    justify-content: space-between;
    align-items: center;

    .ms_card-txt-sx{
        padding: 25px;
        font-weight: bold;
        font-size: 0.9rem;

    }

    .ms_card-txt-dx{
        padding: 20px;
        font-size: 0.8rem;
        color: $colorText11;
    }
}

.col-4.ms_carousel-card{
    background-color: $colorBg1;
    border-radius: 25px;
    width: calc(100% / 3 - 40px);
    margin: 25px 20px;

}

</style>