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
        <div class="grid-wrapper__center col-xs-12 col-md-6">
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
                <a href="#">Investor relations</a>
              </p>
              <p>
                <a href="#">Regulatory information</a>
              </p>
              <p>
                <a href="#">Charity Partnerships</a>
              </p>
              <p>
                <a href="#">Modern Slavery Statement</a>
              </p>
              <p>
                <a href="#">Part VII Transfer</a>
              </p>
              <p>
                <a href="#">Rogue Trader Guidance</a>
              </p>
            </div>
          </div>
        </div>
        <div class="grid-wrapper__right col-xs-12 col-md-3">
          <h3 class="footer-grid-heading">Sign up to our Newsletter</h3>
          <input type="text" class="newsletter-input">
          <a href="#" class="sign-to-newsletter-cta center-xs middle-xs">
            <strong>Sign up</strong>
          </a>
        </div>
      </div>
      <div class="copy">
        Service plans, maintenance & support plans are provided by Domestic & General Services Limited. Insurance policies are provided by Domestic & General Insurance PLC. Domestic & General Insurance PLC is an insurance undertaking, not an intermediary. We are the underwriter of the insurance policies and do not provide a personal recommendation or advice. Domestic & General Insurance PLC is authorised by the Prudential Regulation Authority and regulated by the Financial Conduct Authority and the Prudential Regulation Authority (Financial Services Register Number 202111). Our address and details of our authorisation can be checked on the
        <a href="https://register.fca.org.uk/">FCA website</a> or by contacting the FCA on 0800 111 6768.
      </div>
      <div class="list-wrapper">
        <ul class="footer-list">
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
export default {};
</script>

<style lang="scss">
#footer {
  display: flex;
  background: #f2f2f2;
  a {
    color: #333;
  }
  .container {
    // border:1px solid goldenrod;
    .row {
      &--grid-wrapper {
        margin: 0;
      }
    }
    .grid-wrapper {
      padding: 40px 0;
      text-align: left;

      .footer-grid-heading {
        padding: 20px 0;
        @media (min-width: 768px) {
          font-size: 22px;
          padding-top: 0;
          line-height: 36px;
        }
      }
      &__left {
        // border: 1px solid purple;
        p {
          font-size: 20px;
          line-height: 34px;
        }
      }
      &__center {
        border: none;
        padding-left: 1rem;
        @media (min-width: 1200px) {
          border-left: 1px solid #bcbcbc;
          padding-left: 50px;
        }
      }
      &__right {
        // border: 1px solid purple;
        display: flex;
        flex-direction: column;
        .newsletter-input {
          height: 50px;
          // border-radius: 3px;
          &:focus {
            outline: none;
          }
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
        }
      }
    }
    .copy {
      // border: 1px solid goldenrod;
      color: #666666;
      text-align: left;
      font-size: 14px;
      line-height: 23px;
      padding: 20px;
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
          padding: 5px 20px;

          &:first-child {
            color: #666666;
          }
          a {
            color: #333;
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
