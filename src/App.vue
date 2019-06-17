<template>
  <div id="app">
    <Homepage></Homepage>
  </div>
</template>

<script>
import Homepage from './components/Homepage.vue'

export default {
  name: 'app',
  components: {
    Homepage
  }
}
</script>

<style lang="scss">
 @import "./assets/sass/styles";

#app {
  // font-family: 'Avenir', Helvetica, Arial, sans-serif;
  // -webkit-font-smoothing: antialiased;
  // -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  font-family: 'VAG Rounded W01 Light',sans-serif;

}

// Carousel start
  
.VueCarousel{
  padding-bottom: 90px;
  .VueCarousel-wrapper{
    border-radius: 7px;
    
    box-shadow: 1px 1px 10px 1px #474d96;
    -moz-box-shadow: 1px 1px 10px 1px #474d96;
    -webkit-box-shadow: 1px 1px 10px 1px #474d96;
    .VueCarousel-slide {
      position: relative;
      background: #fff;
      color: #fff;
      font-family: Arial;
      font-size: 24px;
      text-align: center;
      max-height: 90px;
      .slide-brand{
        max-width: 100%;
        max-height: 100%;
      }
    }

    .label {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  }
  .VueCarousel-navigation{
    // display: none;
    
    .VueCarousel-navigation-button{
      top: 25%;
      width: 45px;
      height: 45px;
      background: #E0E0E0;
      border-radius: 50%;
      opacity: 1;
      color: #006DB3;
      // display: none;
      @media(min-width: 768px){
        display: block;
      }
    }
    .VueCarousel-navigation-prev{
      left: 50px;
      @media(min-width: 1100px){
        left:25px;
      }
    }
    .VueCarousel-navigation-next{
      right: 50px;
      @media(min-width: 1100px){
        right: 25px;
      }
    }
    
  }
  .VueCarousel-pagination{
    display: none;
  }
} 
// Carousel end

</style>
