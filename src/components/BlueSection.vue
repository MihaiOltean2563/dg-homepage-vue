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
                <div class="col-xs-12 col-sm-2 benefit__icon">
                  <div class="icon-box center-xs">
                    <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_plan.svg" alt="icon">
                  </div>
                </div>
                <div class="col-xs-12 col-sm-10 benefit__desc top-xs start-xs">
                  <div class="benefit-title">
                    <div>
                      <img class="arr-right" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png">
                    </div>
                   <div>
                      <h2 class="benefit__desc__title"><a href="#">My Account</a></h2>
                   </div>
                  </div>
                  <p class="benefit__desc__description">View and manage your plans anytime,<br> anywhere</p>
                </div>
              </div>
              <div class="row benefit">
                <div class="col-xs-12 col-sm-2 benefit__icon start-xs">
                  <div class="icon-box center-xs">
                    <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/Repair+engineer+icon+outlined.svg" alt="icon">
                  </div>
                </div>
                <div class="col-xs-12 col-sm-10 benefit__desc top-xs start-xs">
                  <div class="benefit-title">
                    <div>
                      <img class="arr-right" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png">
                    </div>
                    <div>
                      <h2 class="benefit__desc__title"><a href="#">Digital repair booking</a></h2>
                    </div>
                  </div>
                  <p class="benefit__desc__description">Request a repair and track existing engineer appointments from any device</p>
                </div>
              </div>
              <div class="row benefit">
                <div class="col-xs-12 col-sm-2 benefit__icon start-xs">
                  <div class="icon-box center-xs">
                    <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/Repair+icon+outlined.svg" alt="icon">
                  </div>
                </div>
                <div class="col-xs-12 col-sm-10 benefit__desc top-xs start-xs">
                  <div class="benefit-title">
                    <div>
                      <img class="arr-right" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png">
                    </div>
                    <div>
                      <h2 class="benefit__desc__title"><a href="#">Troubleshooting and maintenance content</a></h2>
                    </div>
                  </div>
                  <p class="benefit__desc__description">Get quick fixes for common faults without needing an engineer</p>
                </div>
              </div>
            </div>
          </div>
          <div class="col-xs-12 col-md-6 special-warranty__right">
            <div class="img-wrapper">
              <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/father-son.png">
            </div>
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
  a{
    color: #fff;
  }
  .special-warranty-wrapper{
    display: flex;
    .container{ 
      // border: 1px solid goldenrod;
      .special-warranty-title{
        color: #fff;
        font-size: 25px;
        line-height: 38px;
        padding: 90px 20px;
        @media(min-width: 768px){
          font-size: 35px;
          line-height: 52px;
          padding-right:0;
          padding-left:0;
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
                padding-bottom: 20px;
                @media(min-width: 768px){
                  justify-content: center;
                }
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
                padding-top: 5px;
                .benefit-title{
                  display: flex;
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
                  padding-left: 25px;
                }
              }
            }
          }
        }
        &__right{
          // border: 1px solid pink;
          .img-wrapper{
            max-width: 100%;
            max-height: 100%;
            img{
              max-width: 100%;
            }
          }
        }
      }
    }
  }
}
</style>
