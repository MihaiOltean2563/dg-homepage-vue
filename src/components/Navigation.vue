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
      <div class="nav__account-management col-xs-4 middle-xs">
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
    </header>
    <header class="nav-mobile row" role="banner">
      <div class="nav-mobile__burger col-xs-2 start-xs middle-xs">
       <div id="hamburger" @click="display_menu">
					<span></span>
					<span></span>
					<span></span>
				</div>
      </div>
      <div class="nav-mobile__brand col-xs-8 middle-xs center-xs">
        <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/logo_D%2BG_white.png" alt="Domestic&General Logo">
      </div>
      <div class="nav-mobile__basket col-xs-2 center-xs middle-xs">
        Basket
      </div>

       <nav id="menu">
          <div class="nav-link-mobile middle-xs">Get protected</div>
          <div class="nav-link-mobile middle-xs">Book a repair</div>
          <div class="nav-link-mobile middle-xs">Help and advice</div>
        </nav>
    </header>
  </div>
</template>

<script>
// import { Slide } from 'vue-burger-menu'

export default{
  /* eslint-disable */

  name: 'Navigation',
  methods: {
     display_menu(){
      var body = document.getElementsByTagName("body")[0];
			(!body.classList.contains("display_menu")) ? body.classList.add("display_menu") : body.classList.remove("display_menu");
       console.log('display menu fired');
      //  return 1;
    }
  },
  components: {
    // Slide
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
      border: 1px solid goldenrod;
      display: flex;
      max-width: 100%;
      margin: 0;
      #menu{
          width: 100%;
          display: flex;
          height: 0;
          -webkit-transform-origin: 50% 0;
          transform-origin: 50% 0;
          transition: 0.6s ease;
          flex-direction: column;
          .nav-link-mobile{
            opacity: 0;
            height: 0;
            padding-left: 20px;
          }
        }
      a{
        color: #fff;
      }
      &__burger{
        display: flex;
        #hamburger {
          cursor: pointer;
          border-radius: 50%;
          position: absolute;
          // left: 12%;
          // top: 30px;
          // transform: translateY(-50%);
        }
        #hamburger span {
          height: 2px;
          margin-top: 5px;
          margin-bottom: 5px;
          background-color: white;
          display: block;
          transition: 0.33s;
          &:nth-child(1) {width: 12px;}
          &:nth-child(2) {width: 24px;}
          &:nth-child(3) {width: 12px;}
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
      }
    }
  }

  

  .display_menu #hamburger {
    span:nth-child(1) {transform: rotate(45deg) translate(2px, 1px); }
    span:nth-child(2) {transform: rotate(-45deg) ;}
    span:nth-child(3) {transform: rotate(45deg) translate(6px, -9px);}
  }

  .display_menu .nav-mobile #menu .nav-link-mobile{
    opacity: 1;
		display: block;
    height: 20px;
    // border-bottom: 1px solid gray;
    transition: 0.6s ease;
    opacity: 1;
    display: flex;
    flex: 1;
  }
  .display_menu .nav-mobile #menu{
    height:150px;
    background: #fff;
    color: #333;
  }
    
</style>

<!--Working nav component-->
 <!-- <Slide right class="nav-burger-wrapper">
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
  </Slide> -->