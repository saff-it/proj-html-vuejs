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
                <div class="col-3">
        
                    <img class="w-50" src="../assets/img/Group-247.png" alt="Data Analysis">
                    <h5>Data Analysis</h5>
                    <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper</p>
              
                </div>
                <div class="col-3">
        
                    <img class="w-50" src="../assets/img/Group-247.png" alt="Data Analysis">
                    <h5>Data Analysis</h5>
                    <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper</p>
              
                </div>
                <div class="col-3">
        
                    <img class="w-50" src="../assets/img/Group-247.png" alt="Data Analysis">
                    <h5>Data Analysis</h5>
                    <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper</p>
              
                </div>
                <div class="col-3">
        
                    <img class="w-50" src="../assets/img/Group-247.png" alt="Data Analysis">
                    <h5>Data Analysis</h5>
                    <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper</p>
              
                </div>
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

div.container{
    display: flex;
    flex-direction: column;
    align-items: center;
}

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

.col-3{
    display: flex;
    flex-direction: column;
    align-items: center;

    h5{
        font-weight: 600;
        margin-top: 60px
    }

    p{
        font-size: 0.8rem;
        margin-top: 20px;
        font-weight: 300;
        width: 70%;
        text-align: center;
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