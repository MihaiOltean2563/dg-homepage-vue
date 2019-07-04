<template>
  <div id="app">
    <Homepage></Homepage>
  </div>
</template>

<script>
import Homepage from "./components/Homepage.vue";

export default {
  name: "app",
  components: {
    Homepage
  },
  mounted() {
    let trustpilotScript = document.createElement("script");
    trustpilotScript.setAttribute(
      "src",
      "//widget.trustpilot.com/bootstrap/v5/tp.widget.bootstrap.min.js"
    );
    trustpilotScript.setAttribute("async", "true");
    document.head.appendChild(trustpilotScript);
    let googleCDNFont = document.createElement("link");
    googleCDNFont.setAttribute(
      "href",
      "https://fonts.googleapis.com/css?family=Varela+Round&display=swap"
    );
    googleCDNFont.setAttribute("rel", "stylesheet");
    document.head.appendChild(googleCDNFont);
  }
};
</script>

<style lang="scss">
@import "./assets/sass/styles";


#app {
  // font-family: 'Varela Round', sans-serif;
}

.bm-overlay{
  background: transparent;
}

// Carousel start

.VueCarousel {
  padding-bottom: 40px;
  .VueCarousel-wrapper {
    border-radius: 0;
    background: #fff;
    box-shadow: 1px 1px 10px 1px #474d96;
    -moz-box-shadow: 1px 1px 10px 1px #474d96;
    -webkit-box-shadow: 1px 1px 10px 1px #474d96;
    @media(min-width: 768px){
      border-radius: 7px;
    }
    
    .VueCarousel-inner{
      .VueCarousel-slide {
        position: relative;
        background: #fff;
        color: #fff;
        font-family: Arial;
        font-size: 24px;
        text-align: center;
        max-height: 90px;
        padding: 20px 0;
        
        .slide-brand {
          max-width: 100%;
          max-height: 100%;
        }
      }
      .VueCarousel-slide:nth-child(odd){
        display: flex;
        justify-content: flex-end;
        @media(min-width: 500px){
          display: initial;
        }
      }
      .label {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
      }

    }
  }
  .VueCarousel-navigation {
    // display: none;

    .VueCarousel-navigation-button {
      top: 25%;
      width: 45px;
      height: 45px;
      border-radius: 50%;
      opacity: 1;
      color: #006db3;
      background: transparent;
      font-size: 20px;
      @media (min-width: 768px) {
        display: block;
        background: #e0e0e0;
      }
      &:focus{
        outline: none;
      }
    }
    .VueCarousel-navigation-prev {
      left: 50px; //keep 50 so it doesn't create vertical scroll
      @media (min-width: 768px) {
        left: 30px;
      }
      @media (min-width: 1100px) {
        left: 25px;
      }
    }
    .VueCarousel-navigation-next {
      right: 50px; //keep 50 so it doesn't create vertical scroll
       @media (min-width: 768px) {
        right: 30px;
      }
      @media (min-width: 1100px) {
        right: 25px;
      }
    }
  }
  .VueCarousel-pagination {
    display: none;
  }
}
// Carousel end
</style>
