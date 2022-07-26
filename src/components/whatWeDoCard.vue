<template>
    <div class="col-3">

        <img class="w-50" :src="singleCard.pic" :alt="singleCard.title">
        <h5>{{singleCard.title}}</h5>
        <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper</p>

    </div>
</template>

<script>
export default {
    props: ['singleCard'],
}
</script>

<style lang="scss">
@import "../styles/general.scss";
@import "../styles/variables.scss";
@import "../styles/mixins.scss";

.col-3 {
    display: flex;
    flex-direction: column;
    align-items: center;

    h5 {
        font-weight: 600;
        margin-top: 60px
    }

    p {
        font-size: 0.8rem;
        margin-top: 20px;
        font-weight: 300;
        width: 70%;
        text-align: center;
    }
}
</style>