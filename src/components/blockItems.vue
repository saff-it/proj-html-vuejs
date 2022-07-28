<template>
    <div class="ms_upper-txt" :class="{ 'ms_pricing-txt': singleItem.special == true }">
        <span class="ms_block-pretitle">{{singleItem.pretitle}}</span>
        <h2> <span class="ms_bolder-txt">{{singleItem.titleBold}}</span> {{singleItem.titleLight}} </h2>
        <span class="ms_subtitle">{{singleItem.subtitle}}</span>
    </div>
</template>

<script>
export default {
    props: ['singleItem']
}
</script>

<style lang="scss">
@import "../styles/general.scss";
@import "../styles/variables.scss";
@import "../styles/mixins.scss";

.ms_upper-txt {
    text-align: center;
    margin: 70px;

    .ms_block-pretitle {
        color: $colorText9;
    }

    h2 {
        font-size: 3rem;
        margin: 10px;
        font-weight: 400;

        span.ms_bolder-txt {
            font-weight: 900;
        }
    }

    .ms_subtitle{
        font-size: 0.8rem;
    }
}

</style>