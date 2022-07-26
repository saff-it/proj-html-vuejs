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
                <div class="col-3"></div>
            </div>

            <button>View All Services</button>

        </div>
    </section>




  </main>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";
@import "../styles/variables.scss";
@import "../styles/mixins.scss";


.ms_upper-txt{
    text-align: center;
    margin: 70px;

    span:first-child{
        color: $colorText9;
    }

    h2{
        font-size: 3rem;
        margin: 10px;
        font-weight: 400;

        span.ms_bolder-txt{
            font-weight: 900;
            color: black;
        }
    }
}

button {
    @include buttonLayout;
    background-color: $colorText9;
    text-align: center;
}
</style>