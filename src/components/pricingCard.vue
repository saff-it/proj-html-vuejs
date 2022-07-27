<template>
    <div class="ms_pricing-card">

        <h3>{{singlePricingCard.title}}</h3>
        <span class="ms_pricing-subtit">{{singlePricingCard.subtitle}}</span>
        <span class="ms_pricing-dollar">$</span>
        <span class="ms_price-num">{{singlePricingCard.price}}</span>
        <span class="ms_price-per-month">Per month</span>
        <ul>
            <li v-for="(item, index) in pricingCardListItems" :key="index">
            <span>{{item.itemBold}}</span> {{item.itemNormal}}</li>
        </ul>
        <button class="ms_pricing-btn">Order Now <i class="fa-solid fa-arrow-right ms-4"></i> </button>

    </div>
</template>

<script>
export default {
    props: ['singlePricingCard'],

    data: function() {
        return {

            pricingCardListItems: [

                {
                    itemBold: 'Creative',
                    itemNormal: 'Design Enabled',
                },
                {
                    itemBold: 'Vibrant',
                    itemNormal: 'Color Usage',
                },
                {
                    itemBold: 'Eye',
                    itemNormal: 'Catching Design',
                },
                {
                    itemBold: 'Extreme',
                    itemNormal: 'Typography',
                },
                {
                    itemBold: 'Exeptional',
                    itemNormal: 'Design',
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

.ms_pricing-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: white;
    padding: 40px 80px;
    margin: 0 18px;
    border-radius: 20px;

    h3{
        font-weight: 900;
    }

    .ms_pricing-subtit{
        text-transform: uppercase;
        font-size: 0.8rem;
        font-weight: 900;
        margin-bottom: 20px;
    }

    .ms_pricing-dollar{
        font-size: 0.8rem;
        align-self: flex-start;
        padding-left: 20px;
    }

    .ms_price-num{
        font-size: 4rem;
        font-weight: 900;
    }

    .ms_price-per-month{
        font-size: 0.7rem;
    }

    ul{
        list-style: none;
        padding: 0;
        margin: 35px 0;
        text-align: center;
        
        li{
            font-size: 0.8rem;
            margin-bottom: 7px;

            span{
                font-weight: 900;
            }
        }
    }

    button{
    @include buttonLayout;
    background-color: $colorText9;

    }

}
</style>