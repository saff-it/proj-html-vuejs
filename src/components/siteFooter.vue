<template>
  <footer>

    <!-- top footer  -->
    <section class="ms_footer-section">
      <div class="container">
        <div class="row">

          <div class="col-3 ms_lft-clmn">
            <div class="ms_footer-logo">
              <img src="../assets/img/white-logo-2.png" alt="" class="w-100">
            </div>

            <p>When, while the lovely valley teems with vapour around meand the When, while the lovely valley teems with
              vapour around meand the</p>
          </div>

          <div class="col-3 ms_mdle-lft-clmn">

            <h6>Quick Links</h6>
            <ul>
              <li v-for="(link, index) in quickLinks" :key="index">{{ link.link }}</li>
            </ul>

          </div>

          <div class="col-3 ms_mdle-rght-clmn">

            <h6>Resouces</h6>
            <ul>
              <li v-for="(resource, index) in resources" :key="index">{{ resource.link }}</li>
            </ul>

          </div>

          <div class="col-3 ms_rght-clmn">

            <div class="ms_rght-clmn-container">

              <h6>Contact Us</h6>
              <ul>
                <li class="mb-5"> <strong class="text-white"> Address: </strong> Via dei Colli Piacentini</li>
                <li> <strong class="text-white"> Phone: </strong> +39 333 44 55 890</li>
                <li> <strong class="text-white"> Email: </strong> info@boolean.org</li>

              </ul>

            </div>

          </div>



        </div>
      </div>
    </section>

    <!-- bottom footer  -->
    <section class="ms_footer-section-bottom">
      <div class="container ms_bottom-footer-container">

        <div>
          © 2022 Simone. All Rights Reserved.
        </div>

        <div class="bottom-footer-rgt">
          <i class="fa-brands fa-instagram"></i>
          <i class="fa-brands fa-linkedin-in"></i>
          <i class="fa-brands fa-facebook-f"></i>
          <i class="fa-brands fa-twitter"></i>
        </div>
      </div>
    </section>

  </footer>
</template>

<script>
// import whatWeDoCard from './whatWeDoCard.vue'


export default {
  name: 'siteFooter',
  components: {

  },

  data: function () {
    return {

      quickLinks: [

        {
          link: 'Services',
        },

        {
          link: 'Contact',
        },

        {
          link: 'Blog',
        },

      ],

      resources: [

        {
          link: 'Art Design',
        },

        {
          link: 'Computer',
        },

        {
          link: 'IT News',
        },

        {
          link: 'Networking',
        },

        {
          link: 'Security',
        },

      ],

    }
  }



}


</script>

<style lang="scss">
@import "../styles/general.scss";
@import "../styles/variables.scss";
@import "../styles/mixins.scss";

// TOP FOOTER 

.ms_footer-section {
  background-color: $colorBg9;
  

  .container {
    padding-top: 180px;
    padding-bottom: 50px;
  }
}

.ms_lft-clmn {
  color: $colorText11;
  margin: 0;


  .ms_footer-logo {
    align-self: flex-start;
    margin-bottom: 15px;
    width: 40%;
  }

  p {
    text-align: left;
    align-self: flex-start;
    font-size: 0.7rem;
    width: 85%;

  }
}

.ms_mdle-lft-clmn {
  color: white;

  h6 {
    align-self: flex-start;

  }

  ul {
    list-style: none;
    align-self: flex-start;
    padding: 0;


    li {
      font-weight: 100;
      font-size: 0.7rem;
      color: $colorText11;
      margin: 10px 0;

    }
  }
}

.ms_mdle-rght-clmn {
  color: white;

  ul {
    list-style: none;
    align-self: flex-end;
    padding: 0;

    li {
      font-weight: 100;
      font-size: 0.7rem;
      color: $colorText11;
      margin: 10px 0;
      text-align: center;


    }
  }
}

.ms_rght-clmn {
  color: white;

  .ms_rght-clmn-container {
    align-self: flex-end;

    ul {
      list-style: none;
      padding: 0;

      li {
        font-weight: 100;
        font-size: 0.7rem;
        color: $colorText11;
        margin: 10px 0;
        text-align: left;
      }
    }
  }

}

// BOTTOM FOOTER 

.ms_footer-section-bottom{
  background-color: $colorBg9;
  border-top: 0.5px solid $colorBg3;

  .ms_bottom-footer-container{
    @include displayFlex;
    color: $colorText11;
    font-size: 0.7rem;
    height: 40px;

  .bottom-footer-rgt i{
    margin: 0 10px;
    color: white;
  }


  }

}



</style>