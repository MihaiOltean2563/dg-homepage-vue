<template>
  <section id="special-warranty">
    <div class="special-warranty-wrapper center-xs">
      <div class="container">
        <h1 class="special-warranty-title">Take control of your plans with help from Domestic & General, the UK’s leading specialist warranty provider</h1>

        <carousel :scrollPerPage="true" :navigationEnabled="true" :perPageCustom="[[480, 2], [768, 3]]">
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/logo_aeg.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/logo_baxi.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/logo_beko.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/logo_indesit.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/logo_whirlpool.png"></slide>
        </carousel>

        <div class="row special-warranty">
          <div class="col-xs-12 col-md-6 special-warranty__left">
            <div class="benefits-wrapper">
              <div class="row benefit">
                <div class="col-xs-2 benefit__icon center-xs">
                  <div class="icon-box center-xs">
                    <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_plan.svg" alt="icon">
                  </div>
                </div>
                <div class="col-xs-10 benefit__desc top-xs start-xs">
                  <div class="row">
                    <div class="col-xs-1">
                      <img class="arr-right" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png">
                    </div>
                    <div class="col-xs-11">
                      <h2 class="benefit__desc__title">My Account</h2>
                    </div>
                  </div>
                  <p class="benefit__desc__description">View and manage your plans anytime,<br> anywhere</p>
                </div>
              </div>
              <div class="row benefit">
                <div class="col-xs-2 benefit__icon center-xs">
                  <div class="icon-box center-xs">
                    <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/Repair+engineer+icon+outlined.svg" alt="icon">
                  </div>
                </div>
                <div class="col-xs-10 benefit__desc top-xs start-xs">
                  <div class="row">
                    <div class="col-xs-1">
                      <img class="arr-right" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png">
                    </div>
                    <div class="col-xs-11">
                      <h2 class="benefit__desc__title">Digital repair booking</h2>
                    </div>
                  </div>
                  <p class="benefit__desc__description">Request a repair and track existing engineer appointments from any device</p>
                </div>
              </div>
              <div class="row benefit">
                <div class="col-xs-2 benefit__icon center-xs">
                  <div class="icon-box center-xs">
                    <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/Repair+icon+outlined.svg" alt="icon">
                  </div>
                </div>
                <div class="col-xs-10 benefit__desc top-xs start-xs">
                  <div class="row">
                    <div class="col-xs-1">
                      <img class="arr-right" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png">
                    </div>
                    <div class="col-xs-11">
                      <h2 class="benefit__desc__title">Troubleshooting and maintenance content</h2>
                    </div>
                  </div>
                  <p class="benefit__desc__description">Get quick fixes for common faults without needing an engineer</p>
                </div>
              </div>
            </div>
          </div>
          <div class="col-xs-12 col-md-6 special-warranty__right">
              <img src="../assets/coming-soon.png">
          </div>
        </div>

      </div><!--container-end-->
    </div>
   
  </section>
</template>


<script>
import { Carousel, Slide } from 'vue-carousel';

export default {
  name: 'blue-section',
  components:{
    Carousel,
    Slide
  }
}
</script>

<style scoped lang="scss">
#special-warranty{
  background: #006DB3;

  .special-warranty-wrapper{
    display: flex;
    .container{ 
      // border: 1px solid goldenrod;
      .special-warranty-title{
        color: #fff;
        font-size: 25px;
        line-height: 38px;
        padding: 90px 0;
        @media(min-width: 768px){
          font-size: 35px;
          line-height: 52px;
          width: 80%;
          margin: 0 auto;
        }
      }
      
      .special-warranty{
        margin: 0;
        .row{
          margin: 0;
        }
        .col{
          padding: 0;
        }
        &__left{
          // border: 1px solid pink;
          padding: 0;

          .benefits-wrapper{  
            color: #fff;
            .benefit{
              // border: 1px solid wheat;
              padding: 20px 0;
              &__icon{
                // border: 1px solid palegreen;
                display: flex;
                padding-right: 0;
                .icon-box{
                  width: 50px;
                  height: 50px;
                  border-radius: 50%;
                  background: #FFFFFF;
                  display: flex;
                }
              }
              &__desc{
                // border: 1px solid palegreen;
                display: flex;
                flex-direction: column;
                padding-left: 0;
                padding-top: 10px;
                .row{
                  width: 100%;
                  .col-xs-1{
                    padding: 0;
                  }
                  .col-xs-11{
                    padding-left: 0;
                  }
                }
                &__title{
                  font-size: 22px;
                  line-height: 30px;
                  .arrow-right{
                    
                  }
                }
                &__description{
                  font-size: 18px;
                  line-height: 28px;
                }
              }
            }
          }
        }
        &__right{
          // border: 1px solid pink;
        }
      }
    }
  }
}
</style>
