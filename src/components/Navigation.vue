<template>
  <div class="container-fluid nav-wrapper">
    <header class="nav row" role="banner">
      <div class="nav__brand col-xs-2 end-xs">
        <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/logo_D%2BG_white.png" alt="Domestic&General Logo">
      </div>
      <div class="nav__list col-xs-6 middle-xs">
        <ul class="list-wrapper">
          <li class="list-wrapper__item"><a href="#"><strong>Get protected</strong></a></li>
          <li class="list-wrapper__item"><a href="#"><strong>Book a repair</strong></a></li>
          <li class="list-wrapper__item"><a href="#"><strong>Help and advice</strong></a></li>
        </ul>
      </div>
      <div class="nav__account-management col-xs-4 middle-xs">
        <div class="row account-box">
          <a href="#" class="col-xs-6 account-box__login middle-xs end-xs">
            <img class="user-icon" src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/icon_my-account.svg" alt="user-icon">
            <strong>Log in</strong>
          </a>
          <a href="#" class="col-xs-6 account-box__register middle-xs start-xs">
            <strong>Register</strong>
          </a>
        </div>
        <span class="menu-burger">
          <span class="hamburger"></span>
        </span>
      </div>
    </header>
    <header class="nav-mobile row" role="banner">
      <div class="nav-mobile__brand col-xs-10 start-xs">
        <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Header/logo_D%2BG_white.png" alt="Domestic&General Logo">
      </div>
      <div class="nav-mobile__account-management col-xs-2 middle-xs">
        <span class="menu-burger">
          <span class="hamburger"></span>
        </span>
      </div>
    </header>
  </div>
</template>

<script>

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
      @media(min-width: 768px){
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
              padding: 0 15px;
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
      @media(min-width: 768px){
        display: none;
      }
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
            padding: 0 15px;
            font-size: 18px;
            
          }
        }
      }
      &__account-management{
        // border: 1px solid seagreen;
        font-size: 18px;
        display: flex;
        .menu-burger{
          
          position: absolute;
          right: 23px;
          width: 50px;
          height: 50px;
          background: #FFF;
          border-radius: 50% 50% 50% 50%;
          transition: .5s ease-in-out;
          cursor: pointer;
          background: transparent;

          .hamburger{
            position: absolute;
            top: 25px;
            left: 10px;
            width: 30px;
            height: 2px;
            // background: #000;
            background: #fff;
            display: block;
            -webkit-transform-origin: center;
            transform-origin: center;
            transition: .5s ease-in-out;
            &:before,
            &:after{
            transition: .5s ease-in-out;
            content: "";
            position: absolute;
            display: block;
            width: 100%;
            height: 2px;
            background: #fff;
            }
            &:before {
              top: -10px;
            } 
            &:after {
              bottom: -10px;
            }
          }
        }
      }
    }
  }
    
</style>