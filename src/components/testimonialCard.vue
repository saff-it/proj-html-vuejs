<template>
    <div class="col-4 ms_testimonial-container">

        <div class="ms_avatar-box">
            <img class="w-100" :src="require(`../assets/img/${testimonialCard.img}`)" :alt="testimonialCard.name">
        </div>

        <div class="ms_stars-box">
            <i class="fa-solid fa-star ms_full-star "></i>
            <i class="fa-solid fa-star ms_full-star"></i>
            <i class="fa-solid fa-star ms_full-star"></i>
            <i class="bi bi-star ms_empty-star"></i>
            <i class="bi bi-star ms_empty-star"></i>
        </div>

        <p>When, while the lovely valley teems with vapour
            around meanthe while the lovely valley teems with vapou while the lovely valley teems</p>

        <span class="fw-bold">{{testimonialCard.name}}</span>
        <span>{{testimonialCard.job}}</span>

    </div>
</template>

<script>
export default {
    props: ['testimonialCard'],
}
</script>

<style lang="scss">
@import "../styles/general.scss";
@import "../styles/variables.scss";
@import "../styles/mixins.scss";


.col-4.ms_testimonial-container{
    padding: 0 60px;
    display: flex;
    flex-direction: column;
    align-items: center;

    .ms_avatar-box{
        width: 25%;
        border: 5px solid $colorText12;
        border-radius: 50%;
        margin-bottom: 40px;
    }

    .ms_stars-box i{
        font-size: 0.9rem;
        margin: 0 1px;
    }

    .ms_stars-box i.ms_full-star{
        color: $colorText9;
    }

    .ms_stars-box i.ms_empty-star{
        color: $colorText9;
    }

    p{
        text-align: center;
        margin: 25px 0 20px 0;
        font-size: 0.9rem;

    }

    span:last-child{
        font-size: 0.9rem;
        margin-top: 5px;
    }
}
</style>