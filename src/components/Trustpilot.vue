<template>
  <section id="trustpilot">
    <div class="cols-wrapper">
      <div class="trustpilot-wrapper middle-xs">
        <!-- TrustBox widget - Mini --> 
        <div class="trustpilot-widget" data-locale="en-GB" data-template-id="53aa8807dec7e10d38f59f32" data-businessunit-id="4cb3113600006400050dfb02" data-style-height="100px" data-style-width="100%" data-theme="light">    <a href="https://uk.trustpilot.com/review/domesticandgeneral.com" target="_blank" rel="noopener">Trustpilot</a> </div> 
        <!-- End TrustBox widget - Mini-->
      </div>

      <div class="login-account-wrapper middle-xs">
        <div class="wrapper-big-screens middle-xs">
  
          <h2 class="desktop-title" v-if="isNewCustomer">Take control of your plans with <strong>My Account</strong></h2>
          <h2 class="mobile-title main">Take control of your plans with</h2>
          <h2 class="mobile-title"><strong>My Account</strong></h2>
          <h2 v-if="!isNewCustomer">Protect the appliances that matter to you</h2>

          <a v-if="isNewCustomer" class="login-cta center-xs middle-xs" href="https://www.domesticandgeneral.com/AllMyPoliciesView?catalogId=10052&langId=44&storeId=10151">
            <strong>Go to My Account</strong>
          </a>
          <a v-if="!isNewCustomer" class="login-cta center-xs middle-xs" href="#">
            <strong>Get an instant quote</strong>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
 name: 'Trustpilot',
 data(){
   return{
     isNewCustomer: true,
   }
 }

};
</script>

<style lang="scss">
#trustpilot {
   .cols-wrapper{
      display: flex;
      // border: 1px solid goldenrod;
      flex-direction: column;
      @media(min-width: 768px){
        flex-direction: row;
      }
      .trustpilot-wrapper{
        border-right: none;
        border-top: 1px solid #DCDCDC;
        display: flex;
        padding: 20px 0;
        order: 1;
        > .trustpilot-widget{
          flex: 1;
          // border: 1px solid goldenrod;
          @media(min-width: 1800px){
            justify-content: flex-end;
            flex: none;
          }
        }

        @media(min-width: 768px){
          flex-basis: 50%;
          max-width: 50%;
          border-right: 1px solid #DCDCDC;
          border-bottom: none;
          border-top: none;
          order: 0;
        }
        @media(min-width: 1200px){
          justify-content: flex-end;
        }
        @media(min-width: 1800px){
          justify-content: flex-end;
          padding-right: 100px;
        }
      }
      .login-account-wrapper{
        display: flex;
        flex-direction: column;
        padding: 30px 0;
        
        // border: 1px solid goldenrod;
        @media(min-width: 768px){
          flex-basis: 50%;
          max-width: 50%;
          justify-content: flex-start;
        }
        @media(min-width: 1800px){
          align-items: flex-start;
          padding-left: 30px;
        }

        .wrapper-big-screens{
          display: flex;
          flex-direction: column;
          // border: 1px solid goldenrod;;
        }

        h2{
          color: #333333;
          font-weight: 300;
          padding: 0 20px 20px 20px;
          font-size: 18px;
          line-height: 24px;
          // flex: 1 0 auto;
          @media(min-width: 768px){
            font-size: 25px;
            line-height: 28px;
          }
        }
        .mobile-title{
          display: block;
          @media(min-width: 768px){
           display: none;
          }
        }
        .mobile-title.main{
           padding-bottom: 5px;
        }
        .desktop-title{
          display: none;
          @media(min-width: 768px){
           display: block;
          }
        }
       
        .login-cta{
          background: #0a93d3;
          color: #fff;
          height: 50px;
          display: flex;
          border-radius: 3px;
          font-size: 18px;
          padding: 0 15px;
          
          @media (min-width: 300px) {
            width: 280px;
          }
          @media (min-width: 768px) {
            font-size: 22px;
            margin-bottom: 15px;
          }
        }

      }
    }
}
</style>
