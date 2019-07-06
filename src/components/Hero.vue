<template>
  <section id="hero" class="center-xs">
    <div class="container container__wrapper">
      <div class="quote-finder center-xs">
        <div class="quote-finder__widget middle-xs">
          <div class="widget-icon center-xs">
            <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_arrow-purple.svg" alt="arrow-purple">
          </div>
          <div class="widget-body middle-xs">
            <p><strong>Received a letter in the post?</strong></p>
            <a class="find-my-quote" id="find-my-quote" href="#">
              <strong>Find my quote</strong>
            </a>
          </div>
        </div>
      </div>
      <div class="welcome-intro middle-xs">
        <div class="welcome-intro-wrapper">
          <h1 class="welcome-intro__title" v-if="isNewCustomer">Protect the appliances that matter to you</h1>
        </div>
        <a class="btn welcome-intro__cta center-xs middle-xs" href="https://www.domesticandgeneral.com/products" v-if="isNewCustomer">Get an instant quote</a>
      </div>
    </div>
    <!--container-wrapper-end-->
  </section>
</template>

<script>
export default {
  data(){
    return{
     isNewCustomer: true,
    }  
  },
};
</script>

<style lang="scss">

#hero {
  display: flex;
  background: url("https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/img_banner-gradient.png");
  background-repeat: no-repeat;
  background-size: cover;

  .container__wrapper {
    // border: 1px solid goldenrod;
    .welcome-intro {
      display: flex;
      flex-direction: column;

      &__title {
        color: #fff;
        font-size: 28px;
        padding: 20px 10px;
        max-width: 300px;
        margin: 0 auto;
        letter-spacing: 2px;
        line-height: 38px;
        font-family: 'VAG Rounded W01 Bold',sans-serif;
        font-weight: bold;
        @media (min-width: 550px) {
          padding-left: 0;
          padding-right: 0;
          padding: 60px 0;
          max-width: 455px;
          font-size: 42px;
          line-height: 62px;
        }
    
      }
      &__cta {
        background: #0a93d3;
        color: #fff;
        height: 50px;
        display: flex;
        border-radius: 3px;
        font-size: 18px;
        margin-bottom: 30px;
        padding: 0 15px;
        transition: 300ms background cubic-bezier(0.4, 0, 0.6, 1);
        -webkit-transition: 300ms background cubic-bezier(0.4, 0, 0.6, 1);
        font-family: 'VAG Rounded W01 Bold',sans-serif;
        letter-spacing: .5px;
        @media (min-width: 300px) {
          width: 280px;
        }
        @media (min-width: 768px) {
          font-size: 22px;
          margin-bottom: 100px;
        }
        &:hover{
          background: #006db3;
          -webkit-transition: 300ms background cubic-bezier(0.4, 0, 0.6, 1);
          transition: 300ms background cubic-bezier(0.4, 0, 0.6, 1);
        }
      }
    }

    .quote-finder {
      display: flex;
      margin: 130px 0 0 0;
      font-family: 'VAG Rounded W01 Bold',sans-serif;

      &__widget {
        display: flex;
        border-radius: 50px;
        padding: 5px 15px;
        padding-left: 8px;
        padding-bottom: 6px;
        background: rgba(255, 255, 255, 0.18);
        p,
        a {
          color: #fff;
          letter-spacing: .5px;
        }
        p {
          padding: 0 10px;
          margin: 5px 0;
          color: #D8CCE0;
          font-size: 14px;
          margin-bottom: 3px;
          @media (min-width: 768px) {
            font-size: 16px;
            margin-bottom: 5px;
          }
        }
        .widget-icon {
          border-radius: 50%;
          width: 40px;
          height: 40px;
          background: #4c2178;
          display: flex;
          img{
            width: 18px;
            @media (min-width: 768px) {
               width: 14px;
            }
          }
          @media (min-width: 768px) {
            width: 25px;
            height: 25px;
          }
        }
        .widget-body {
          display: block;
          text-align: left;

          @media (min-width: 500px) {
            display: flex;
          }
        }
        .find-my-quote {
          text-decoration: underline;
          padding-left: 10px;
          padding-right: 10px;
          @media (min-width: 768px) {
            padding-left: 0;
          }
        }
      }
    }
  }
}
</style>
