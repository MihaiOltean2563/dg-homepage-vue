<template>
  <footer id="footer" class="center-xs">
    <div class="container">
      <div class="grid-wrapper row row--grid-wrapper">
        <div class="grid-wrapper__left col-xs-12 col-md-3">
          <h3 class="footer-grid-heading">Products we protect</h3>
          <p>
            <a href="https://www.domesticandgeneral.com/products/household">Household appliances</a>
          </p>
          <p>
            <a href="https://www.domesticandgeneral.com/heating">Heating</a>
          </p>
          <p>
            <a href="https://www.domesticandgeneral.com/products/tv-audio">TV & Audio</a>
          </p>
          <p>
            <a href="https://www.domesticandgeneral.com/products/camera-mobile">Photo & Video devices</a>
          </p>
        </div>
        <div class="grid-wrapper__center col-xs-12 col-md-5">
          <h3 class="footer-grid-heading">Useful links</h3>
          <div class="row">
            <div class="col-xs-12 col-md-5">
              <p>
                <a href="https://www.domesticandgeneral.com/corporate/about-us">About us</a>
              </p>
              <p>
                <a href="https://www.domesticandgeneral.com/content/help-advice-section/faq">Help and advice</a>
              </p>
              <p>
                <a href="https://www.domesticandgeneral.com/content/contact-domestic-general">Contact us</a>
              </p>
              <p>
                <a href="https://www.domesticandgeneral.com/content/help-advice-section/corporate-information/media-centre">Media centre</a>
              </p>
              <p>
                <a href="https://careers.domesticandgeneral.com/">Careers</a>
              </p>
            </div>
            <div class="col-xs-12 col-md-7">
              <p>
                <a href="https://investors.domesticandgeneral.com/">Investor relations</a>
              </p>
              <p>
                <a href="https://www.domesticandgeneral.com/company-information-legal">Regulatory information</a>
              </p>
              <p>
                <a href="https://www.domesticandgeneral.com/content/help-advice-section/corporate-information/charity-partnerships">Charity Partnerships</a>
              </p>
              <p>
                <a href="https://www.domesticandgeneral.com/modern-slavery">Modern Slavery Statement</a>
              </p>
              <p>
                <a href="https://www.domesticandgeneral.com/PartVIITransfer">Part VII Transfer</a>
              </p>
              <p>
                <a href="https://www.domesticandgeneral.com/content/help-advice-section/faq/received-a-strange-call-">Rogue Trader Guidance</a>
              </p>
            </div>
          </div>
        </div>
        <div class="grid-wrapper__right col-xs-12 col-md-4">
          <h3 class="footer-grid-heading">Sign up to our Newsletter</h3>
          <input type="text" class="newsletter-input" v-model="emailNewsletter">
          <a @click="signToNewsLetter" class="sign-to-newsletter-cta center-xs middle-xs">Sign up</a>
          <p v-if="hasSubmitted">Thank you, you have subscribed.</p>
        </div>
      </div>
      <div class="copy row">
        <div class="col-xs-12">
          Service plans, maintenance & support plans are provided by Domestic & General Services Limited. Insurance policies are provided by Domestic & General Insurance PLC. Domestic & General Insurance PLC is an insurance undertaking, not an intermediary. We are the underwriter of the insurance policies and do not provide a personal recommendation or advice. Domestic & General Insurance PLC is authorised by the Prudential Regulation Authority and regulated by the Financial Conduct Authority and the Prudential Regulation Authority (Financial Services Register Number 202111). Our address and details of our authorisation can be checked on the
          <a href="https://register.fca.org.uk/">FCA website</a> or by contacting the FCA on 0800 111 6768.
        </div>
      </div>
      <div class="list-wrapper row">
        <ul class="footer-list col-xs-12">
              <li>© 2019 Domestic & General Group Limited</li>
              <li>
                <a href="https://www.domesticandgeneral.com/web-terms-conditions">Website Terms and Conditions</a>
              </li>
              <li>
                <a href="https://www.domesticandgeneral.com/privacy-cookies-policy">Privacy and Cookies policy</a>
              </li>
              <li>
                <a href="https://www.domesticandgeneral.com/accessibility">Accessibility policy</a>
              </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
 /* eslint-disable */

export default {
  data(){
    return{
      emailNewsletter: '',
      hasSubmitted: false
    }
  },
  watch: {
    'emailNewsletter': function(val, oldVal){
      var oldNewsletterInputElem = document.getElementById('newsletterEmail');
      if(!oldNewsletterInputElem !== null){
        oldNewsletterInputElem.value = val;
      }
    }
  },
  methods: {
    signToNewsLetter(){
      var err = document.getElementById('newsletterMessage');
      var email = document.getElementById('newsletterEmail').value;
      var regex = /[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}/i;
      
      if(regex.test(email)){
        console.log('signing');
        this.hasSubmitted = true;
        var newsLetterInputEl = document.querySelector('.newsletter-input');
        var newsLetterCtaEl = document.querySelector('.sign-to-newsletter-cta');
        newsLetterInputEl.style.display = 'none';
        newsLetterCtaEl.style.display = 'none';
        var oldEl = document.getElementById('newsletterForm');
        var oldSubmit = oldEl.querySelector('[type=submit]');
        oldSubmit.click();
      }else{
        console.log('errorrrrrr');
        return;
      }
    }
  }
};
</script>

<style lang="scss">
#footer {
  display: flex;
  background: #f2f2f2;
  max-width: initial!important;

  a, h3 {
    color: #333;
  }
  .container {
    // border:1px solid goldenrod;
    .grid-wrapper {
      padding: 40px 0;
      margin: 0;
      text-align: left;
      @media(min-width: 768px){
        padding: 65px 0;
      }
      .footer-grid-heading {
        padding-top: 0;
        padding: 20px 0;
        font-family: 'VAG Rounded W01 Bold',sans-serif;
        font-size: 22px;
        line-height: 36px;

        @media (min-width: 768px) {
          padding-top: 0;
        }
      }
      &__left {
        // border: 1px solid purple;
        .footer-grid-heading {
          padding-top: 0;
        }
        p {
          font-size: 20px;
          line-height: 34px;
          a{
            font-family: 'VAG Rounded W01 Light',sans-serif;
          }
        }
      }
      &__center {
        border: none;
        padding-left: 1rem;
        padding-top: 40px;
        a{
          font-family: 'VAG Rounded W01 Light',sans-serif;
          &:hover{
            text-decoration: underline;
          }
        }
        @media (min-width: 768px) {
          padding-top: 0;
        }
        @media (min-width: 1200px) {
          border-left: 1px solid #bcbcbc;
          padding-left: 50px;
        }
        .footer-grid-heading {
            padding-top: 0;
        }
      }
      &__right {
        // border: 1px solid purple;
        display: flex;
        flex-direction: column;
        .newsletter-input {
          height: 45px;
          border-radius: 3px;
          border: 1px solid #DCDCDC;
          padding-left: 5px;
          &:focus {
            outline: none;
          }
        }
        .newsletter-old-input{
          margin-top: 10px;
        }
        .sign-to-newsletter-cta {
          height: 50px;
          background: #0a93d3;
          color: #fff;
          width: 100%;
          margin-top: 20px;
          font-size: 18px;
          line-height: 36px;
          display: flex;
          border-radius: 3px;
          font-family: 'VAG Rounded W01 Bold',sans-serif;
          letter-spacing: 1px;
          transition: 300ms background cubic-bezier(0.4, 0, 0.6, 1);
          -webkit-transition: 300ms background cubic-bezier(0.4, 0, 0.6, 1);
          &:hover{
            background: #561d80;
            -webkit-transition: 300ms background cubic-bezier(0.4, 0, 0.6, 1);
            transition: 300ms background cubic-bezier(0.4, 0, 0.6, 1);
            cursor: pointer; 
          }
        }
      }
    }
    .copy {
      // border: 1px solid goldenrod;
      color: #666666;
      text-align: left;
      font-size: 14px;
      line-height: 23px;
      padding-bottom: 30px;
      font-family: Arial, Helvetica, sans-serif;
      margin: 0;
      a {
        text-decoration: underline;
      }
      @media (min-width: 768px) {
        font-size: 16px;
        line-height: 28px;
      }
    }
    .list-wrapper {
      // border: 1px solid goldenrod;
      padding: 20px 0;
      margin: 0;
      @media(min-width: 990px){
        margin: 0;
      }
      .footer-list {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        text-align: left;
        @media (min-width: 990px) {
          flex-direction: row;
        }
        li {
          font-size: 14px;
          line-height: 23px;
          padding: 5px 0;

          &:first-child {
            color: #666666;
            font-family: Arial, Helvetica, sans-serif;
            padding-bottom: 40px;
            @media(min-width: 990px){
              padding-bottom: 0;
            }
          }
          a {
            color: #333;
            font-family: 'VAG Rounded W01 Light',sans-serif;

            &:hover{
              text-decoration: underline;
            }
          }
          @media (min-width: 990px) {
            font-size: 16px;
            line-height: 28px;
            padding: 0;
            padding-right: 20px;
          }
        }
      }
    }
  }
}
</style>
