<template>
  <div class="container-fluid nav-wrapper">
    <header class="nav row" role="banner">
      <div class="nav__brand col-xs-2 end-xs">
        <a href="https://www.domesticandgeneral.com">
          <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/logo_D%2BG_white.png" alt="Domestic&General Logo">
        </a>
      </div>
      <div class="nav__list col-xs-6 middle-xs">
        <ul class="list-wrapper">
          <li class="list-wrapper__item"><a href="https://www.domesticandgeneral.com/products"><strong>Get protected</strong></a></li>
          <li class="list-wrapper__item"><a href="https://www.domesticandgeneral.com/repairs"><strong>Book a repair</strong></a></li>
          <li class="list-wrapper__item"><a href="https://www.domesticandgeneral.com/content/help-advice-section/faq"><strong>Help and advice</strong></a></li>
        </ul>
      </div>
      <div class="nav__account-management col-xs-4 middle-xs" v-if="!isNewCustomer">
        <div class="row account-box">
          <a href="#" class="col-xs-6 account-box__login middle-xs end-xs">
            <img class="user-icon" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_my-account.svg" alt="User Icon">
            <strong>Log in</strong>
          </a>
          <a href="#" class="col-xs-6 account-box__register middle-xs start-xs">
            <strong>Register</strong>
          </a>
        </div>
      </div>
      <div v-if="isNewCustomer" class="nav__account-management col-xs-4 middle-xs">
         <a href="#"  class="col-xs-12 account-box__login middle-xs end-xs new-customer">
            <img class="user-icon" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_my-account.svg" alt="User Icon">
            <strong>My account</strong>
          </a>
      </div>
    </header>
    <header class="nav-mobile row" role="banner">
      <div class="nav-mobile__burger col-xs-2 start-xs middle-xs">

        <Slide class="nav-burger-wrapper">
          <a id="home" href="https://www.domesticandgeneral.com/content/help-advice-section/faq">
            <span>Get protected</span>
          </a>
          <a id="home" href="https://www.domesticandgeneral.com/repairs">
            <span>Book a repair</span>
          </a>
          <a id="home" href="https://www.domesticandgeneral.com/content/help-advice-section/faq">
            <span>Help and advice</span>
          </a>
          <a id="home" href="#">
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
        <a href="#">
          <img class="basket-img" src="../assets/images/basket.svg" alt="Basket Icon">
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
    }  
  },
  mounted(){
    this.cloneBasketNode();
  },
  methods: {
    display_menu(){
      var body = document.getElementsByTagName("body")[0];
			(!body.classList.contains("display_menu")) ? body.classList.add("display_menu") : body.classList.remove("display_menu");
       console.log('display menu fired');
    },
    cloneBasketNode(){
      console.log('Basket node was cloned!')
      // var nodeToClone = document.querySelector('.svg-icon--minibasket');
      // console.log('nodetoclone', nodeToClone)
    }
  },
  components: {
    Slide
  }
}
</script>

<style lang="scss">
  .nav-wrapper{
    position: absolute;
    left: 0;
    right: 0;
    margin-top: 35px;
    
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
            &__item{
              padding: 0 10px;
              font-size: 18px;
              
            }
          }
        }
        &__account-management{
          // border: 1px solid seagreen;
          font-size: 18px;
          display: flex;
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
