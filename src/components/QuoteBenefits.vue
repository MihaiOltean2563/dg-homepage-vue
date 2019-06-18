<template>
  <section id="quote-benefits">
    <div class="quote-benefits-wrapper center-xs">
      <div class="container">
        <div class="row qb-wrapper">
          <div class="qb-wrapper__left col-xs-12 col-md-6">
            <h2 class="quote-title">We've got you covered</h2>
            <p
              class="quote-copy"
            >Our insurance policies protect the products you can’t live without, keeping your home running and giving you added peace of mind.</p>
            <a href="#" class="get-quote-cta center-xs middle-xs">
              <strong>Get a quote</strong>
            </a>
          </div>
          <div class="qb-wrapper__right col-xs-12 col-md-6">
            <div class="benefits-wrapper">
              <div class="benefit-row">
                  <div class="icon-wrapper">
                    <img
                      class="arr-right"
                      src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/white-tick.svg"
                    >
                  </div>
                <div>
                  <h5 class="benefit__desc__title">
                    <strong>Protection against breakdowns</strong>
                  </h5>
                </div>
              </div>
              <div class="benefit-row">
                  <div class="icon-wrapper">
                    <img
                      class="arr-right"
                      src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/white-tick.svg"
                    >
                  </div>
                <div>
                  <h5 class="benefit__desc__title">
                    <strong>Accidental damage cover</strong>
                  </h5>
                </div>
              </div>
              <div class="benefit-row">
                  <div class="icon-wrapper">
                    <img
                      class="arr-right"
                      src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/white-tick.svg"
                    >
                  </div>
                <div>
                  <h5 class="benefit__desc__title">
                    <strong>Unlimited repairs by expert engineers</strong>
                  </h5>
                </div>
              </div>
              <div class="benefit-row">
                <div class="icon-wrapper">
                    <img
                      class="arr-right"
                      src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/white-tick.svg"
                    >
                </div>
                <div>
                  <h5 class="benefit__desc__title">
                    <strong>Parts, labour, and call-out charges included</strong>
                  </h5>
                </div>
              </div>
              <div class="benefit-row">
                  <div class="icon-wrapper">
                    <img
                      class="arr-right"
                      src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Blue+section/white-tick.svg"
                    >
                  </div>
                <div>
                  <h5 class="benefit__desc__title">
                    <strong> A replacement product if yours can't be fixed</strong>
                    (just pay the cost of installation and disposal)
                  </h5>
                  <a
                    href="#"
                    class="select-boiler-link"
                  >Select your boiler to see the benefits of our maintenance and support plans.</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="social left-xs center-sm">
      <div class="container">
        <div class="social-bar-wrapper">
          <div class="social__follow-us">
            <a href="#">Follow us</a>
          </div>
          <div class="social__twitter center-xs middle-xs">
            <a href="#">
              <img
                src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Footer/icon_social-twitter.svg"
                alt="twitter"
              >
            </a>
          </div>
          <div class="social__facebook center-xs middle-xs">
            <a href="#">
              <img
                src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Footer/icon_social-facebook.svg"
                alt="facebook"
              >
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
#quote-benefits {
  border: none;
  border-bottom: 1px solid #bcbcbc;
   
  .quote-benefits-wrapper {
    display: flex;
    .container {
      // border: 1px solid goldenrod;
      .qb-wrapper {
        margin: 0;
        text-align: left;
        padding-top: 90px;
        padding-bottom: 50px;

        &__left {
          .quote-title {
            font-size: 25px;
            line-height: 32px;
            padding-bottom: 20px;
            @media (min-width: 768px) {
              font-size: 35px;
              line-height: 44px;
            }
          }
          .quote-copy {
            @media (min-width: 600px) {
              width: 60%;
            }
          }
          .get-quote-cta {
            height: 50px;
            background: #561d80;
            border-radius: 3px;
            color: #fff;
            width: 100%;
            margin: 40px 0;
            font-size: 18px;
            line-height: 36px;
            display: flex;
            @media (min-width: 600px) {
              max-width: 320px;
            }
          }
        }
        &__right {
          .benefits-wrapper {
            .benefit-row{
              display: flex;
              padding-bottom: 10px;
              a {
                text-decoration: underline;
                color: #333;
              }
            }
            .icon-wrapper {
              width: 25px;
              height: 25px;
              min-width: 25px;
              min-height: 25px;
              margin-right: 20px;
              img {
                padding: 5px;
              }
            }
            .arr-right {
              background: #0071bb;
              border-radius: 50%;
              position: relative;
              right: 2px;
              width: 100%;
              height: 100%;
            }
            .row {
             
            }

            .benefit__desc__title {
              font-size: 18px;
              line-height: 27px;
              font-weight: normal;
              padding-bottom: 20px;
              @media (min-width: 768px) {
                line-height: 27px;
              }
            }
          }
        }
      }
    }
  }
  .social {
    display: flex;
    padding: 40px 20px;
    background: #f2f2f2;
    .container {
      // border: 1px solid goldenrod;
      .social-bar-wrapper {
        display: flex;
        @media (min-width: 768px) {
          padding-left: 1rem;
        }
      }
    }
    &__follow-us {
      font-size: 22px;
      line-height: 36px;
      padding-right: 30px;
      a {
        color: #333;
      }
    }
    &__twitter {
      margin-right: 30px;
      width: 50px;
      height: 50px;
      background: #fff;
      border-radius: 50%;
      display: flex;
      img {
        width: 25px;
        height: 25px;
      }
    }
    &__facebook {
      width: 50px;
      height: 50px;
      background: #fff;
      border-radius: 50%;
      display: flex;
      img {
        width: 25px;
        height: 25px;
      }
    }
  }
}
</style>
