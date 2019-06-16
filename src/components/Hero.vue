<template>
  <section id="hero" class="center-xs">
    <div class="container container__wrapper">
      <div class="quote-finder center-xs">
        <div class="quote-finder__widget middle-xs">
          <div class="widget-icon center-xs">
            <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_arrow-purple.svg" alt="arrow-purple">
          </div>
          <p><strong>Received a letter in the post?</strong></p>
          <a class="find-my-quote" id="find-my-quote" href="#"><strong>Find my quote</strong></a>
        </div>
      </div>
      <div class="welcome-intro middle-xs">
        <h1 class="welcome-intro__title">Manage your plans, appliances, and repairs all in one place</h1>
        <a class="welcome-intro__cta center-xs middle-xs" href="#">Log in to My Account</a>
      </div>
    </div><!--container-wrapper-end-->
  </section>
</template>

<script>
export default {
  
}
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
        padding-top: 20px;
        padding-bottom: 50px;
        @media (min-width: 768px) {
          font-size: 42px;
          width: 60%;
        }
      }
      &__cta {
        background: #0a93d3;
        color: #fff;
        height: 55px;
        width: 280px;
        display: flex;
        border-radius: 3px;
        font-size: 18px;
        margin-bottom: 100px;
        @media (min-width: 768px) {
          font-size: 22px;
        }
      }
    }
  
    .quote-finder {
      
      display: flex;
      margin: 150px 0 40px 0;
      &__widget{
        display: flex;
        border-radius: 50px;
        padding: 10px;
        background: rgba(255, 255, 255, 0.18);
        p, a{
          color: #fff;
        }
        p{
          padding: 0 10px;
        }
        .widget-icon{
          border-radius: 50%;
          width: 25px;
          height: 25px;
          background: #4C2178;
          display: flex;
        }
        .find-my-quote{
          text-decoration: underline;
          padding-right: 10px;
        }
      }
    }
    
  }
  
}

</style>
