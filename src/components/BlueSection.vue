<template>
  <section id="special-warranty">
    <div class="special-warranty-wrapper center-xs">
      <div class="container">
        <h1 class="special-warranty-title">Take control of your plans with help from Domestic & General, the UK’s leading specialist warranty provider</h1>

        <carousel
          :scrollPerPage="true"
          :navigationEnabled="true"
          :perPageCustom="[[480, 2],[600, 3], [768, 4], [960, 5]]"
          
        >
        <!-- :autoplay="true" -->
          <slide><img class="slide-brand" src="../assets/images/Brands/AEG.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/AO.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Baxi.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Beko.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Belling.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Blomberg.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Bosch.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Brand_logos.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Bush.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Candy.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Dimplex.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Electrolux.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Flavel.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Game.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Glow-worm.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Hoover.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Hotpoint.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Ideal.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Indesit.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Jessops.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Leisure.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/LG.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Main-heating.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Miele.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Mira-showers.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Neff.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Potterton.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Samsung.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Scottish-power.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Siemens.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Sky.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Stoves.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Vaillant.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Valor.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Vokera.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Whirlpool.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Worcester-bosch.png"></slide>
          <slide><img class="slide-brand" src="../assets/images/Brands/Zanussi.png"></slide>
        </carousel>

        <div class="row special-warranty">
          <div class="col-xs-12 col-md-6 special-warranty__left">
            <div class="benefits-wrapper">
              <a href="https://www.domesticandgeneral.com/AllMyPoliciesView?catalogId=10052&langId=44&storeId=10151">
                <div class="row benefit">
                  <div class="col-xs-12 col-sm-2 benefit__icon">
                    <div class="icon-box center-xs">
                      <img
                        src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_plan.svg"
                        alt="icon"
                      >
                    </div>
                  </div>
                  <div class="col-xs-12 col-sm-10 benefit__desc top-xs start-xs">
                    <div class="benefit-title">
                      <img class="arr-right" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png">
                      <div>
                        <h2 class="benefit__desc__title">
                          <a href="#">My Account</a>
                        </h2>
                      </div>
                    </div>
                    <p class="benefit__desc__description">
                      View and manage your plans anytime,
                      <br>anywhere
                    </p>
                  </div>
                </div>
              </a>
              <a href="https://www.domesticandgeneral.com/repairs">
                <div class="row benefit">
                  <div class="col-xs-12 col-sm-2 benefit__icon start-xs">
                    <div class="icon-box center-xs">
                      <img
                        src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/Repair+engineer+icon+outlined.svg"
                        alt="icon"
                      >
                    </div>
                  </div>
                  <div class="col-xs-12 col-sm-10 benefit__desc top-xs start-xs">
                    <div class="benefit-title">
                        <img class="arr-right"
                          src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png"
                        >
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
              <a href="https://www.domesticandgeneral.com/content/help-advice-section/faq">
                <div class="row benefit">
                  <div class="col-xs-12 col-sm-2 benefit__icon start-xs">
                    <div class="icon-box center-xs">
                      <img
                        src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/Repair+icon+outlined.svg"
                        alt="icon"
                      >
                    </div>
                  </div>
                  <div class="col-xs-12 col-sm-10 benefit__desc top-xs start-xs">
                    <div class="benefit-title">
                      <div class="last-benefit-icon">
                        <img
                          class="arr-right"
                          src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/icon_arrow-white.png"
                        >
                      </div>
                      <div>
                        <h2 class="benefit__desc__title">
                          <a href="https://www.domesticandgeneral.com/content/help-advice-section/faq">Troubleshooting and maintenance content</a>
                        </h2>
                      </div>
                    </div>
                    <p
                      class="benefit__desc__description"
                    >Get quick fixes for common faults without needing an engineer</p>
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
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "blue-section",
  components: {
    Carousel,
    Slide
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
        padding: 90px 20px;
        @media (min-width: 768px) {
          font-size: 35px;
          line-height: 52px;
          padding-right: 0;
          padding-left: 0;
          max-width: 975px;
          margin: 0 auto;
        }
      }

        .special-warranty {
        margin: 0;
        padding: 0 10px;
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
            .benefit {
              // border: 1px solid wheat;
              padding: 20px 0;
              &__icon {
                // border: 1px solid palegreen;
                display: flex;
                padding-right: 0;
                padding-bottom: 20px;
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
                .benefit-title {
                  display: flex;
                  transition: .5s ease-out;
                  &:hover > img{
                    transform: translateX(3px);
                    transition: .5s ease-out;
                  }
                  &:hover > .last-benefit-icon{
                    transform: translateX(3px);
                    transition: .5s ease-out;
                  }
                }
                &__title {
                  font-size: 22px;
                  line-height: 30px;
                 
                }
                &__description {
                  font-size: 18px;
                  line-height: 28px;
                  padding-left: 25px;
                }
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
