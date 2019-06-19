<template>
  <section id="trustpilot">
    <div class="cols-wrapper">
      <div class="trustpilot-wrapper middle-xs">
        <!-- <div
            class="trustpilot-widget"
            data-locale="en-GB"
            data-template-id="5406e65db0d04a09e042d5fc"
            data-businessunit-id="4cb3113600006400050dfb02"
            data-style-height="40px"
            data-style-width="100%"
            data-theme="light">
            <a
              href="https://uk.trustpilot.com/review/domesticandgeneral.com"
              target="_blank"
              rel="noopener"
            >Trustpilot</a>
          </div> -->
          <!-- <div class="trustpilot-widget" data-locale="en-GB" data-template-id="5419b6ffb0d04a076446a9af" data-businessunit-id="4cb3113600006400050dfb02" data-style-height="150px" data-style-width="100%" data-theme="light"> <a href="https://uk.trustpilot.com/review/domesticandgeneral.com" target="_blank" rel="noopener">Trustpilot</a> </div> -->
      <!-- TrustBox widget - Micro Combo --> 
      <!-- <div class="trustpilot-widget" data-locale="en-GB" data-template-id="5419b6ffb0d04a076446a9af" data-businessunit-id="4cb3113600006400050dfb02" data-style-height="100px" data-style-width="70%" data-theme="light"> <a href="https://uk.trustpilot.com/review/domesticandgeneral.com" target="_blank" rel="noopener">Trustpilot</a> 
      </div>  -->
      <!-- End TrustBox widget -->

      <!-- TrustBox widget - Mini --> 
      <div class="trustpilot-widget" data-locale="en-GB" data-template-id="53aa8807dec7e10d38f59f32" data-businessunit-id="4cb3113600006400050dfb02" data-style-height="120px" data-style-width="100%" data-theme="light"> <a href="https://uk.trustpilot.com/review/domesticandgeneral.com" target="_blank" rel="noopener">Trustpilot</a> </div> 
      <!-- End TrustBox widget -->
      </div>
      <div class="login-account-wrapper middle-xs">
        <h2>Take control of your plans with <strong>My Account</strong></h2>
        <a class="login-cta center-xs middle-xs" href="#">
          <strong>Log in to My Account</strong>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {

// API Key: PnGH3ryOxEs13oR4MpzMvO4IYmeY6I0g
// Secret: Dm8c7AhGTPVAAtMN

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
        border-bottom: 1px solid #BCBCBC;
        display: flex;
        padding: 30px 0;
        > .trustpilot-widget{
          flex: 1;
          > *{
            font-size: 20px!important;
          }
        }
        @media(min-width: 768px){
          flex-basis: 50%;
          max-width: 50%;
          border-right: 1px solid #BCBCBC;
          border-bottom: none;
        }
      }
      .login-account-wrapper{
        // border: 1px solid darkgreen;
        display: flex;
        flex-direction: column;
        padding: 40px 0;
        h2{
          color: #333333;
          font-weight: 300;
          padding: 0 20px 20px 20px;
          @media(min-width: 768px){
            // padding-right: 0;
            // padding-left: 0;
          }
        }
        @media(min-width: 768px){
           flex-basis: 50%;
          max-width: 50%;
        }
        .login-cta{
          background: #0a93d3;
          color: #fff;
          height: 55px;
          display: flex;
          border-radius: 3px;
          font-size: 18px;
          margin-top: 20px;
          padding: 0 15px;
          @media (min-width: 300px) {
            width: 280px;
          }
          @media (min-width: 768px) {
            font-size: 22px;
          }
        }

      }
    }
}
</style>
