<template>
  <div class="container-fluid nav-wrapper" :class="{ sticky: showNavbar}">

    <header class="nav row" role="banner">
      <div class="nav__brand col-xs-2 end-xs">
        <a href="https://www.domesticandgeneral.com">
          <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/logo_D%2BG_white.png" alt="Domestic&General Logo">
        </a>
      </div>
      <div class="nav__list col-xs-7 middle-xs">
        <ul class="list-wrapper">
          <li class="list-wrapper__item"><a href="https://www.domesticandgeneral.com/products">Get protected</a></li>
          <li class="list-wrapper__item"><a href="https://www.domesticandgeneral.com/repairs">Book a repair</a></li>
          <li class="list-wrapper__item"><a href="https://www.domesticandgeneral.com/content/help-advice-section/faq">Help and advice</a></li>
        </ul>
      </div>
      <div v-if="isNewCustomer" class="nav__account-management col-xs-3 middle-xs">
         <a href="https://www.domesticandgeneral.com/AllMyPoliciesView?catalogId=10052&langId=44&storeId=10151"  class="col-xs-12 account-box__login middle-xs end-xs new-customer">
            <img class="user-icon" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_my-account.svg" alt="User Icon">
            My account
          </a>
          <a href="#" class="logout-cta" v-if="showLogoutCta">Logout</a>
      </div>
    </header>

    <header class="nav-mobile row" role="banner">
      <div class="nav-mobile__burger col-xs-2 start-xs middle-xs">

        <Slide class="nav-burger-wrapper">
          <a id="home" href="https://www.domesticandgeneral.com/content/help-advice-section/faq">
            <span>Get protected</span>
          </a>
          <a id="repairs" href="https://www.domesticandgeneral.com/repairs">
            <span>Book a repair</span>
          </a>
          <a id="help-advice" href="https://www.domesticandgeneral.com/content/help-advice-section/faq">
            <span>Help and advice</span>
          </a>
          <a id="logout" href="#">
            <span>Log out</span>
          </a>
        </Slide>

      </div>
      <div class="nav-mobile__brand col-xs-8 middle-xs center-xs">
        <a href="https://www.domesticandgeneral.com">
          <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/logo_D%2BG_white.png" alt="Domestic&General Logo">
        </a>
      </div>
      <div class="nav-mobile__basket col-xs-2 center-xs middle-xs">
        <a href="https://www.domesticandgeneral.com/AllMyPoliciesView?catalogId=10052&langId=44&storeId=10151">
          <img class="user-icon" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_my-account.svg" alt="User Icon">
        </a>
      </div>

    </header>
  </div>
</template>

<script>
import { Slide } from 'vue-burger-menu'

export default{
  /* eslint-disable */
  name: 'Navigation',

  data(){
    return{
     isNewCustomer: true,
     showNavbar: false,
     showLogoutCta: true
    }  
  },
  components: {
    Slide
  },
  mounted(){
    this.isLoggedIn();
  },
  methods:{
    handleScroll(){
      window.pageYOffset > 0 ? 
        this.showNavbar = true :
        this.showNavbar = false;
    },
    isLoggedIn(){
      // check for existance of  elem with id 'signInOutQuickLink'
      var loggedInElem = document.getElementById('signInOutQuickLink');
      // console.log('loggedInElem', loggedInElem);
      if(loggedInElem !== null){
        showLogoutCta = true;
      }
    }
  },
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll);
  }
}
</script>

<style lang="scss">
  .nav-wrapper{
    position: absolute;
    left: 0;
    right: 0;
    padding-top: 35px;
    background: transparent;
    transition: .5s ease-in-out;
    &.sticky{
      position:fixed;
      top:0;
      width: 100%;
      padding-top: 10px;
      padding-bottom: 10px;
      // background: #400668;
      background: rgba(64, 6, 104, .92);
      z-index: 1;
      @media(min-width: 768px){
        position: absolute;
        top: initial;
        background: transparent;
      }
    }
    @media(min-width: 1200px){
      max-width: 1200px; 
    }
    .nav{
      display: none;
      @media(min-width: 975px){
        // border: 1px solid goldenrod;
        display: flex;
        color: #fff;
        max-width: 100%;
        margin: 0;
        a{
          color: #fff;
        }
        &__brand{
          // border: 1px solid seagreen;
          display: flex;
          padding-right: 40px;       
          img{
            max-height: 50px;
          }
        }
        &__list{
          // border: 1px solid seagreen;
          display: flex;
          padding-left: 0;

          .list-wrapper{
            display: flex;
            list-style: none;
            border-left : .5px solid whitesmoke;
            padding: 5px 0 5px 0;
            a{
              font-family: 'VAG Rounded W01 Bold',sans-serif;
              transition: 300ms color cubic-bezier(0.4, 0, 0.6, 1);
              -webkit-transition: 300ms color cubic-bezier(0.4, 0, 0.6, 1);
              letter-spacing: .5px;
              &:hover{
                color: hsla(0,0%,100%,.7);
                -webkit-transition: 300ms color cubic-bezier(0.4, 0, 0.6, 1);
                transition: 300ms color cubic-bezier(0.4, 0, 0.6, 1);
              }
            }
            &__item{
              // padding: 0 10px;
              padding-right: 40px;
              font-size: 18px;
              &:first-of-type{
                padding-left: 40px;
              }
            }
          }
        }
        &__account-management{
          // border: 1px solid seagreen;
          font-size: 18px;
          display: flex;
          a{
            font-family: 'VAG Rounded W01 Bold',sans-serif;
             transition: 300ms color cubic-bezier(0.4, 0, 0.6, 1);
            -webkit-transition: 300ms color cubic-bezier(0.4, 0, 0.6, 1);
             &:hover{
                color: hsla(0,0%,100%,.7);
                -webkit-transition: 300ms color cubic-bezier(0.4, 0, 0.6, 1);
                transition: 300ms color cubic-bezier(0.4, 0, 0.6, 1);
              }
          }
          .logout-cta{
            color: #d8cce0;
          }
          .account-box{
            flex: 1;
            &__login{
              display: flex;
              border-right: .5px solid whitesmoke;
              .user-icon{
                padding-right: 10px;
                max-height: 35px;
              }
            }
            &__login.new-customer{
               border-right: none;
            }
            &__register{
              display: flex;
            }
          }
          
        }
      }
    }
    .nav-mobile{
      @media(min-width: 975px){
        display: none;
      }
      // border: 1px solid goldenrod;
      display: flex;
      max-width: 100%;
      margin: 0;
      position: relative;
   
   
      &__burger{
        display: flex;
        // vue-burger-menu css
        .nav-burger-wrapper{
           .bm-burger-button {
              width: 36px;
              height: 30px;
              left: 0px;
              top: 12px;
              cursor: pointer;
            }
            
            .bm-burger-bars {
              background-color: #fff;
            }
            .line-style {
              position: absolute;
              height: 20%;
              left: 0;
              right: 0;
            }
            .cross-style {
              position: absolute;
              top: 12px;
              right: 2px;
              cursor: pointer;
            }
            .bm-cross {
              background: #bdc3c7;
            }
            .bm-cross-button {
              height: 24px;
              width: 24px;
            }
            .bm-menu {
              height: 100%; /* 100% Full-height */
              width: 0; /* 0 width - change this with JavaScript */
              position: fixed; /* Stay in place */
              z-index: 1000; /* Stay on top */
              top: 0;
              left: 0;
              background-color: rgb(63, 63, 65); /* Black*/
              overflow-x: hidden; /* Disable horizontal scroll */
              padding-top: 60px; /* Place content 60px from the top */
              transition: 0.5s; /*0.5 second transition effect to slide in the sidenav*/
            }

            .bm-overlay {
              background: rgba(0, 0, 0, 0.3);
            }
            .bm-item-list {
              color: #b8b7ad;
              margin-left: 10%;
              font-size: 20px;
              width: 300px;
            }
            .bm-item-list > * {
              display: flex;
              text-decoration: none;
              padding: 0.7em;
            }
            .bm-item-list > * > span {
              margin-left: 10px;
              font-weight: 700;
              color: white;
            }
        }
        // vue-burger-menu css end
        &:hover{
          cursor: pointer; 
        }
      }

      &__brand{
        // border: 1px solid seagreen;
        display: flex;       
        img{
          max-height: 50px;
        }
      }
      &__basket{
        display: flex;
        .basket-img{
          width: 40px;
        }
      }
    }
  }

    
</style>
