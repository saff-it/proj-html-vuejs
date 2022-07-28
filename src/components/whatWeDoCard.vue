<template>
    <div class="col-3">
        <div class="ms_img-box-wwd">
            <img :src="require(`../assets/img/${singleCardWeDo.pic}`)" :alt="singleCardWeDo.title">
        </div>
        
        <h5>{{singleCardWeDo.title}}</h5>
        <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper</p>

    </div>
</template>

<script>
export default {
    props: ['singleCardWeDo'],
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
    
    .ms_img-box-wwd{
        width: 50%;
        height: 100px;

        img{
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
    }

    h5 {
        font-weight: 600;
        margin-top: 40px
    }

    p {
        font-size: 0.8rem;
        margin-top: 10px;
        font-weight: 300;
        width: 70%;
        text-align: center;
    }
}
</style>