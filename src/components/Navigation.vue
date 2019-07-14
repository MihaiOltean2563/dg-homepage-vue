<template>
  <div class="nav-wrapper">
    <!-- container-fluid from nav-wrapper above -->
    <header class="nav row" role="banner">
      <div class="nav__brand col-xs-2 end-xs">
        <a href="https://www.domesticandgeneral.com">
          <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/logo_D%2BG_white.png" alt="Domestic&General Logo">
        </a>
      </div>
      <div class="nav__list col-xs-7 middle-xs">
        <ul class="list-wrapper">
          
          <li data-ga-label="Get Protected"
          @click="handleAnalytics" 
          class="list-wrapper__item">
            <a href="https://www.domesticandgeneral.com/products">Get protected</a>
          </li>

          <li data-ga-label="Book Repair"
          @click="handleAnalytics"  
          class="list-wrapper__item">
            <a href="https://www.domesticandgeneral.com/repairs">Book a repair</a>
          </li>
          <li data-ga-label="Help and Advice"
          @click="handleAnalytics"  
          class="list-wrapper__item">
            <a href="https://www.domesticandgeneral.com/content/help-advice-section/faq">Help and advice</a>
          </li>

        </ul>
      </div>
      <div v-if="isNewCustomer" class="nav__account-management col-xs-3 middle-xs" data-ga-label="LoginRegister">
         <a href="https://www.domesticandgeneral.com/AllMyPoliciesView?catalogId=10052&langId=44&storeId=10151"  
         class="account-box__login middle-xs end-xs new-customer"
         @click="handleAnalytics">
            <img class="user-icon" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_my-account.svg" alt="User Icon">
            My account
          </a>
          <a class="logout-cta js__account-link logOut" @click="logout" v-if="showLogoutCta">Logout</a>
      </div>
    </header>

    <header class="nav-mobile row" role="banner">
      <div class="nav-mobile__burger col-xs-2 start-xs middle-xs" :class="{ sticky: showNavbar}">

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
          <a id="logout"
          class="js__account-link logOut"
          @click="logout"
          v-if="showLogoutCta">
            <span>Log out</span>
          </a>
          <a id="my-account" href="https://www.domesticandgeneral.com/AllMyPoliciesView?catalogId=10052&langId=44&storeId=10151">
            <span class="my-account-side-nav">
              My account
              <img class="user-icon" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_my-account.svg" alt="User Icon">
            </span>
          </a>
        </Slide>

      </div>
      <div class="nav-mobile__brand col-xs-8 middle-xs center-xs">
        <a href="https://www.domesticandgeneral.com">
          <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/logo_D%2BG_white.png" alt="Domestic&General Logo">
        </a>
      </div>
      <div class="nav-mobile__basket col-xs-2 center-xs middle-xs">
        <a href="https://www.domesticandgeneral.com/AllMyPoliciesView?catalogId=10052&langId=44&storeId=10151" class="center-xs">
          <img class="user-icon" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_my-account.svg" alt="User Icon">
        </a>
      </div>

    </header>

    <header role="banner" class="nav-slide-in" :class="{ sticky: showNavbar}">
      <div class="row">

        <div class="nav-mobile__burger col-xs-2 start-xs middle-xs">

          <!-- <Slide class="nav-burger-wrapper">
            <a id="home" href="https://www.domesticandgeneral.com/content/help-advice-section/faq">
              <span>Get protected</span>
            </a>
            <a id="repairs" href="https://www.domesticandgeneral.com/repairs">
              <span>Book a repair</span>
            </a>
            <a id="help-advice" href="https://www.domesticandgeneral.com/content/help-advice-section/faq">
              <span>Help and advice</span>
            </a>
            <a id="logout"
            class="js__account-link logOut"
            @click="logout"
            v-if="showLogoutCta">
              <span>Log out</span>
            </a>
            <a id="my-account" href="https://www.domesticandgeneral.com/AllMyPoliciesView?catalogId=10052&langId=44&storeId=10151">
              <span class="my-account-side-nav">
                My account
                <img class="user-icon" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_my-account.svg" alt="User Icon">
              </span>
            </a>
          </Slide> -->

        </div>
        <div class="nav-mobile__brand col-xs-8 middle-xs center-xs">
          <a href="https://www.domesticandgeneral.com">
            <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/logo_D%2BG_white.png" alt="Domestic&General Logo">
          </a>
        </div>
        <div class="nav-mobile__basket col-xs-2 center-xs middle-xs">
          <a href="https://www.domesticandgeneral.com/AllMyPoliciesView?catalogId=10052&langId=44&storeId=10151" class="center-xs">
            <img class="user-icon" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_my-account.svg" alt="User Icon">
          </a>
        </div>
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
     showLogoutCta: false
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
      if(loggedInElem !== null){
        this.showLogoutCta = true;
      }
    },
    logout(){
      var loggedInElem = document.getElementById('signInOutQuickLink');
      if(loggedInElem !== null){
        loggedInElem.click();
      }
    },
    handleAnalytics(e){
      window.dataLayer.push({
        event: 'gaEvent',
        event_action: 'Interaction',
        event_category: 'Header',
        event_label: e.srcElement.parentElement.dataset.gaLabel
      })
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
    // padding-top: 20px;
    background: transparent;
    transition: .5s ease-in-out;

    @media(min-width: 1200px){
      // max-width: 1200px;
      max-width: 100%;
    }
    &.sticky{
      position:fixed;
      top:0;
      width: 100%;
      padding-top: 10px;
      padding-bottom: 10px;
      background: rgba(64, 6, 104, .92);
      z-index: 1;

      @media(min-width: 768px){
        position: absolute;
        top: initial;
        background: transparent;
      }
    }
    .nav{
      display: none;
      padding: 20px 0;
      
      @media(min-width: 975px){
        // border: 1px solid goldenrod;
        display: flex;
        color: #fff;
        // max-width: 100%;
        margin: 0;
        
        a{
          color: #fff;
        }
        &__brand{
          // border: 1px solid seagreen;
          display: flex;
                 
          img{
            max-height: 40px;

            @media(min-width: 1200px){
              max-height: 50px;
            }
          }
          @media(min-width: 1200px){
            padding-right: 40px;
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
              font-size: 18px;
              @media(min-width: 975px) and (max-width: 1200px){
                padding: 0 20px;
              }
              @media(min-width: 1200px){
                padding: 0 20px;
              }
              &:first-of-type{
                @media(min-width: 1200px){
                  padding-left: 40px;
                }
              }
            }
          }
        }
        &__account-management{
          // border: 1px solid seagreen;
          font-size: 18px;
          display: flex;
          padding:0;
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
            padding-left: 20px
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
      @media(min-width: 1200px){
        max-width: 1100px;
        margin: 0 auto;
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
      padding: 20px 0;
   
      &__burger{
        display: flex;
        
        // vue-burger-menu css
        .nav-burger-wrapper{
            position: fixed;
            top: -10px;
            z-index: 1000;
           .bm-burger-button {
              width: 36px;
              height: 30px;
              left:10px;
              cursor: pointer;
            }
            
            .bm-burger-bars {
              background-color: #fff;
            }
            .line-style {
              position: absolute;
              height: 13%;
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
              a:nth-last-child(2){
                padding-bottom: 25px;
              }
              #my-account{
                display: flex;
                align-items: center;
                border-top: 1px solid #d3d3d3;
                .my-account-side-nav{
                  display: flex;
                  align-items: center;
                  img{
                    padding-left: 10px;
                  }
                }
              }
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
        a{
          display: flex;
        }
        display: flex;       
        img{
          max-height: 45px;
        }
      }
      &__basket{
        display: flex;
        a{
          display: flex;
        }
        .basket-img{
          width: 40px;
        }
      }
    }

    .nav-slide-in{
      position: fixed!important;
      top: 0;
      z-index: 100;
      width: 100%;
      opacity: 0;
      display: block;
      -webkit-transition: all 400ms ease-in-out;
      -o-transition: all 400ms ease-in-out;
      transition: all 400ms ease-in-out;
      -webkit-transform: translate3d(0,-60px,0);
      transform: translate3d(0,-60px,0);
      @media(min-width: 975px){
        display: none;
      }
      &.sticky{
        -webkit-box-shadow: 0 0.3rem 0.3rem rgba(0,0,0,.2);
        box-shadow: 0 0.3rem 0.3rem rgba(0,0,0,.2);
        opacity: 1;
        // background: rgba(64, 6, 104, .92);
        background: rgba(64, 6, 104, 1);
        -webkit-transform: translate3d(0,0,0);
        transform: translate3d(0,0,0);
        padding: 10px;
        padding-bottom: 20px;
      }
    }
  }

    
</style>
