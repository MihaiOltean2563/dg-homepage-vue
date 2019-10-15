<template>
  <section id="hero" class="center-xs">
    <div class="container container__wrapper">
      <div class="quote-finder center-xs">
        <div class="quote-finder__widget middle-xs">
          <div class="widget-icon center-xs">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20.82 14.3"><defs></defs><title>post</title><g id="Layer_2" data-name="Layer 2"><g id="Layer_1-2" data-name="Layer 1"><path class="cls-1" d="M19.54,0H1.28A1.28,1.28,0,0,0,0,1.28V13A1.27,1.27,0,0,0,1.28,14.3H19.54A1.27,1.27,0,0,0,20.82,13V1.28A1.28,1.28,0,0,0,19.54,0ZM14.17,7.58A.57.57,0,0,0,14,8a.56.56,0,0,0,.12.4l.07.07,4.31,4.3H2.35l4.3-4.29a.55.55,0,0,0,.07-.78A.53.53,0,0,0,6,7.58l-.07.06L1.58,12V2.44L9.9,7.83a1,1,0,0,0,1,0l8.32-5.39V12L15,7.65a.62.62,0,0,0-.38-.2A.57.57,0,0,0,14.17,7.58Zm-3.76-.72L2.26,1.57h16.3Z"/></g></g></svg>
          </div>
          <div class="widget-body middle-xs">
            <p>Received a letter in the post?</p>
            <!-- <a class="find-my-quote" 
            id="find-my-quote"
            @click="handleAnalytics"
            data-ga-action="FormSubmit"
            data-ga-label="offerSubmit-clicked" 
            href="/find-your-quote">Find my quote</a> -->
          </div>
          <!-- <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_arrow-purple.svg" alt="arrow-purple"> -->
          <a class="find-my-quote" 
            id="find-my-quote"
            @click="handleAnalytics"
            data-ga-action="FormSubmit"
            data-ga-label="offerSubmit-clicked" 
            href="/find-your-quote">

            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="20" height="20" viewBox="0 0 14 13">
              <defs>
                <clipPath id="clip-Artboard_5">
                  <rect width="14" height="13"/>
                </clipPath>
              </defs>
              <g id="Artboard_5" data-name="Artboard – 5" clip-path="url(#clip-Artboard_5)">
                <path id="arrow-right2" d="M7.8,11.8l3.333-3.333a.644.644,0,0,0,0-.933L7.8,4.2a.66.66,0,0,0-.933.933l2.2,2.2h-6.4a.667.667,0,1,0,0,1.333h6.4l-2.2,2.2a.644.644,0,0,0,0,.933A.644.644,0,0,0,7.8,11.8Z" transform="translate(0.5 -1.5)" fill="#fff" stroke="#fff" stroke-width="1"/>
              </g>
            </svg>
          </a>

        </div>
      </div>
      <div class="welcome-intro middle-xs">
        <div class="welcome-intro-wrapper">
          <h1 class="welcome-intro__title" v-if="isNewCustomer">Protect the appliances that matter to you</h1>
        </div>
        <a class="btn welcome-intro__cta center-xs middle-xs" 
        href="/products" 
        v-if="isNewCustomer"
        @click="handleAnalytics" 
        data-ga-action="GetAQuoteButtonClicked"
        data-ga-label="primaryButtons-CTA"
        >Get an instant quote</a>
      </div>
    </div>
    <!--container-wrapper-end-->
  </section>
</template>

<script>
/* eslint-disable */
export default {
  data(){
    return{
      isNewCustomer: true,
    }
  },
  methods: {
    handleAnalytics(e){
      window.dataLayer.push({
        event: 'gaEvent',
        event_action: e.srcElement.dataset.gaAction,
        event_category: 'Home',
        event_label: e.srcElement.dataset.gaLabel
      })
    }
  }
};
</script>

<style lang="scss">

#hero {
  display: flex;
  background: url('https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Hero/img_banner_320.png');
  background-repeat: no-repeat;
  background-size: cover;
  @media(min-width: 640px){
    background: url('https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Hero/img_banner_640.png');
    background-repeat: no-repeat;
    background-size: cover;
  }
  @media(min-width: 990px){
    background: url('https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Hero/img_banner-big.png');
    background-repeat: no-repeat;
    background-size: cover;
  }
  .container__wrapper {
    // border: 1px solid goldenrod;
    .welcome-intro {
      display: flex;
      flex-direction: column;

      &__title {
        color: #fff;
        font-size: 28px;
        padding: 30px 10px;
        max-width: 300px;
        margin: 0 auto;
        letter-spacing: 2px;
        line-height: 38px;
        font-family: 'VAG Rounded W01 Bold',sans-serif;
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
          margin-bottom: 110px;
        }
        &:hover{
          background: #0071bb;
          -webkit-transition: 300ms background cubic-bezier(0.4, 0, 0.6, 1);
          transition: 300ms background cubic-bezier(0.4, 0, 0.6, 1);
        }
      }
    }

    .quote-finder {
      display: flex;
      margin: 100px 0 0 0;
      font-family: 'VAG Rounded W01 Bold',sans-serif;
      @media(min-width: 768px){
        margin: 130px 0 0 0;
      }
      &__widget {
        display: flex;
        border-radius: 50px;
        padding: 5px 15px;
        padding-left: 8px;
        background: rgba(255, 255, 255, 0.18);
        p,
        a {
          color: #fff;
          letter-spacing: .7px;
          font-family: 'VAG Rounded W01 Bold',sans-serif;
        }
        p {
          padding: 0 10px;
          margin: 5px 0;
          font-size: 12px;
          @media (min-width: 768px) {
            font-size: 16px;
            margin-bottom: 5px;
          }
        }
        .widget-icon {
          border-radius: 50%;
          width: 35px;
          height: 35px;
          background: #4c2178;
          display: flex;

          svg{
            width: 20px;
            fill: #fff;
          }

          img{
            width: 18px;
            @media (min-width: 768px) {
               width: 14px;
            }
          }
          @media (min-width: 768px) {
            // width: 25px;
            // height: 25px;
          }
        }
        .widget-body {
          display: block;
          text-align: left;
          a{
            font-family: 'VAG Rounded W01 Bold',sans-serif;
          }
          P{
            font-family: 'VAG Rounded W01 Light',sans-serif;
          }
          @media (min-width: 500px) {
            display: flex;
          }
        }
        .find-my-quote {
          text-decoration: underline;
          padding-left: 10px;
          padding-right: 10px;
          display: flex;
          @media (min-width: 768px) {
            padding-left: 0;
          }
        }
      }
    }
  }
}
</style>
