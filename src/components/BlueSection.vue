<template>
  <section id="special-warranty">
    <div class="special-warranty-wrapper center-xs">
      <div class="container">
        <h1 class="special-warranty-title">Take control of your plans with help from Domestic & General, the UK’s leading specialist warranty provider</h1>

        <carousel
          :scrollPerPage="true"
          :navigationEnabled="true"
          :perPageCustom="[[480, 2],[600, 3], [768, 4], [960, 6]]">
        <!-- :autoplay="true" -->
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/AEG.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/AO.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Baxi.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Beko.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Belling.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Blomberg.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Bosch.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Brand_logos.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Bush.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Candy.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Dimplex.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Electrolux.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Flavel.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Game.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Glow-worm.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Hoover.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Hotpoint.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Ideal.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Indesit.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Jessops.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Leisure.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/LG.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Main-heating.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Miele.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Mira-showers.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Neff.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Potterton.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Samsung.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Scottish-power.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Siemens.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Sky.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Stoves.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Vaillant.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Valor.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Vokera.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Whirlpool.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Worcester-bosch.png"></slide>
          <slide><img class="slide-brand" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Brands-Images/Zanussi.png"></slide>
        </carousel>

        <div class="row special-warranty">
          <div class="col-xs-12 col-md-6 special-warranty__left">
            <div class="benefits-wrapper">
              <a @click="handleAnalytics"
              data-ga-label="LoginRegister"
               href="https://www.domesticandgeneral.com/AllMyPoliciesView?catalogId=10052&langId=44&storeId=10151">
                <div class="row benefit">
                  <div class="col-xs-12 col-sm-2 benefit__icon">
                    <div class="icon-box center-xs">
                      <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_plan.svg" alt="icon">
                    </div>
                  </div>
                  <div class="col-xs-12 col-sm-10 benefit__desc top-xs start-xs">
                    <div class="benefit-title">
                      <img class="arr-right" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png">
                      <div>
                        <h2 class="benefit__desc__title">My Account</h2>
                      </div>
                    </div>
                    <p class="benefit__desc__description">
                      View and manage your plans anytime,
                      <br>anywhere
                    </p>
                  </div>
                </div>
              </a>
              <a @click="handleAnalytics" 
              data-ga-label="Get Protected"
              href="https://www.domesticandgeneral.com/repairs">
                <div class="row benefit">
                  <div class="col-xs-12 col-sm-2 benefit__icon start-xs">
                    <div class="icon-box center-xs">
                      <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/Repair+engineer+icon+outlined.svg" alt="icon">
                    </div>
                  </div>
                  <div class="col-xs-12 col-sm-10 benefit__desc top-xs start-xs">
                    <div class="benefit-title">
                      <img class="arr-right" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png">
                      <div>
                        <h2 class="benefit__desc__title">
                          <a href="https://www.domesticandgeneral.com/repairs">Digital repair booking</a>
                        </h2>
                      </div>
                    </div>
                    <p
                      class="benefit__desc__description"
                    >Request a repair and track existing engineer appointments from any device</p>
                  </div>
                </div>
              </a>
              <a 
              @click="handleAnalytics" 
              data-ga-label="Help and Advice"
              href="https://www.domesticandgeneral.com/content/help-advice-section/faq">
                <div class="row benefit">
                  <div class="col-xs-12 col-sm-2 benefit__icon start-xs">
                    <div class="icon-box center-xs">
                      <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/Repair+icon+outlined.svg" alt="icon">
                    </div>
                  </div>
                  <div class="col-xs-12 col-sm-10 benefit__desc top-xs start-xs">
                    <div class="benefit-title">
                      <div class="last-benefit-icon">
                        <img class="arr-right" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png">
                      </div>
                      <div>
                        <h2 class="benefit__desc__title">
                          <a href="https://www.domesticandgeneral.com/content/help-advice-section/faq">Troubleshooting and maintenance content</a>
                        </h2>
                      </div>
                    </div>
                    <p class="benefit__desc__description">Get quick fixes for common faults without needing an engineer</p>
                  </div>
                </div>
              </a>
            </div>
          </div>
          <div class="col-xs-12 col-md-6 special-warranty__right">
            <div class="img-wrapper">
              <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/father-son.png">
            </div>
          </div>
        </div>
      </div>
      <!--container-end-->
    </div>
  </section>
</template>


<script>
/* eslint-disable */
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "blue-section",
  components: {
    Carousel,
    Slide
  },
  methods: {
    handleAnalytics(e){
      window.dataLayer.push({
        event: 'gaEvent',
        event_action: 'Interaction-Body',
        event_category: 'Home',
        event_label: e.currentTarget.dataset.gaLabel
      })
    }
  }
};
</script>

<style scoped lang="scss">
#special-warranty {
  background: #006db3;
  a {
    color: #fff;
  }
  .special-warranty-wrapper {
    display: flex;
    .container {
      // border: 1px solid goldenrod;
      .special-warranty-title {
        color: #fff;
        font-size: 25px;
        line-height: 38px;
        padding: 60px 30px 50px 30px;
        font-family: 'VAG Rounded W01 Bold',sans-serif;
        letter-spacing: 1px;
        @media (min-width: 768px) {
          font-size: 35px;
          line-height: 52px;
          padding-right: 0;
          padding-left: 0;
          max-width: 975px;
          margin: 0 auto;
          padding: 70px 20px;
        }
      }

      .special-warranty {
        margin: 0;
        padding: 0 30px;
    
        .row {
          margin: 0;
        }
        .col {
          padding: 0;
        }
        &__left {
          // border: 1px solid pink;
          padding: 0;

          .benefits-wrapper {
            color: #fff;
            a{
              display: block;
            }
            .benefit {
              // border: 1px solid wheat;
              padding: 15px 0;
              &:hover{
                .benefit-title img{
                    transform: translateX(3px);
                    transition: .5s ease-out;
                  }
              }
              &__icon {
                // border: 1px solid palegreen;
                display: flex;
                padding-right: 0;
                padding-bottom: 20px;
                opacity: .8;
                @media (min-width: 768px) {
                  justify-content: center;
                }
                .icon-box {
                  width: 50px;
                  height: 50px;
                  border-radius: 50%;
                  background: #ffffff;
                  display: flex;
                }
              }
              &__desc {
                // border: 1px solid palegreen;
                display: flex;
                flex-direction: column;
                padding-left: 0;
                padding-top: 5px;
                font-family: 'VAG Rounded W01 Light',sans-serif;
                .benefit-title {
                  display: flex;
                  transition: .5s ease-out;
                }
                &__title {
                  font-size: 22px;
                  line-height: 30px;
                  font-family: 'VAG Rounded W01 Bold',sans-serif;
                  letter-spacing: 1.5px;
                }
                &__description {
                  font-size: 18px;
                  line-height: 28px;
                  padding-left: 10px;
                  font-family: Arial, Helvetica, sans-serif;
                  letter-spacing: 1px;
                }
              }
              @media(min-width: 768px){
                padding: 30px 0;
              }
            }
          }
        }
        &__right {
          // border: 1px solid pink;
          .img-wrapper {
            max-width: 100%;
            max-height: 100%;
            img {
              max-width: 100%;
            }
          }
        }
      }
    }
  }
}
</style>
