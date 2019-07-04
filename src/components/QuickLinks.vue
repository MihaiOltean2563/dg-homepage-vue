<template>
  <section id="quick-links">
    <div class="quick-links-wrapper center-xs">
      <div class="container">
        <h1 class="quick-links-greeting">
          <strong>Keep your home running smoothly</strong>
        </h1>
        <div class="quick-links-wrapper between-sm">
          <div id="3576035" class="appliance" data-type="washing-machine">
            <a class="appliance__link-wrapper" href="https://www.domesticandgeneral.com/goal-search/household-en/washing-machine-protection">
              <p><strong>Protect your</strong></p>
              <p class="copy--blue"><strong>washing machine</strong></p>
              <div class="img-wrapper">
                <div class="bottom-left">
                  <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Quick+Links/img_washing-machine.png" alt="Washing Machine">
                </div>
              </div>
            </a>
          </div>
          <div id="8261695" class="appliance" data-type="dishwasher">
            <a class="appliance__link-wrapper" href="https://www.domesticandgeneral.com/goal-search/household-en/dishwasher-protection">
              <p><strong>Protect your</strong></p>
              <p class="copy--blue"><strong>dishwasher</strong></p>
              <div class="img-wrapper">
                <div class="bottom-left">
                  <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Quick+Links/img_dishwasher.png" alt="Dishwasher">
                </div>
              </div>
            </a>
          </div>
          <div id="2688671" class="appliance" data-type="fridge-freezer">
            <a class="appliance__link-wrapper" href="https://www.domesticandgeneral.com/goal-search/household-en/fridge-freezer-44">
              <p><strong>Protect your</strong></p>
              <p class="copy--blue"><strong>fridge freezer</strong></p>
              <div class="img-wrapper">
                <div class="bottom-left">
                  <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Quick+Links/img_fridge-freezer.png" alt="Fridge Freezer">
                </div>
              </div>
            </a>
          </div>
          <div id="6165187" class="appliance" data-type="all-appliances">
            <a class="appliance__link-wrapper" href="https://www.domesticandgeneral.com/products">
             <p><strong>View our</strong></p>
              <p class="copy--blue"><strong>appliances</strong></p>
              <div class="img-wrapper">
                <div class="bottom-left">
                  <img src="https://front-end-assets.s3.eu-west-2.amazonaws.com/DGX+-+Homepage/Quick+Links/img_all-appliances.png" alt="All appliaces">
                </div>
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
#quick-links {
  background: #eaeaea;

  .quick-links-wrapper {
    @media (min-width: 768px) {
      display: flex;
    }
    .container{
      // border: 1px solid goldenrod;
      padding-bottom: 90px;

      .quick-links-greeting {
        font-size: 25px;
        line-height: 30px;
        color: #333333;
        padding: 40px 20px;
        @media (min-width: 768px) {
          font-size: 35px;
          line-height: 49px;
          padding: 90px 20px;
        }
      }

      .quick-links-wrapper {
        // border: 1px solid goldenrod;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
        padding: 0 10px;
        @media (min-width: 768px) {
          padding: 0;
        }
        .appliance {
          height: 200px;
          background: #fff;
          box-shadow: 1px 1px 10px 1px #c0c1cc;
          -moz-box-shadow: 1px 1px 10px 1px #c0c1cc;
          -webkit-box-shadow: 1px 1px 10px 1px #c0c1cc;
          flex-basis: 45%;
          max-width: 45%;
          display: flex;
          transition: all 0.3s ease-in-out;
          border-radius: 5px;
          @media (min-width: 1000px) {
            flex-basis: 23%;
            max-width: 23%;
            margin-top: 0;
          }

          &__link-wrapper{
            width: 100%;
            display: flex;
            flex-direction: column;
            padding: 20px 0 0 20px;
            position: relative;
            p{
              text-align: left;
              margin: 0;
            }
            p:first-child{
              color: #333;
              font-size: 14px;
              line-height: 28px;
              @media(min-width: 768px){
                font-size: 18px;
                line-height: 28px;
              }
            }
            .copy--blue{
              color: #0071BB;
              margin: 0;
              flex: 1 0 auto;
              font-size: 16px;
              line-height: 28px;
               @media(min-width: 768px){
                font-size: 22px;
                line-height: 28px;
              }
            }
            .img-wrapper{
              // border: 1px solid goldenrod;
              // border: 1px solid goldenrod;
              height: 100%;
              display: flex;
              .bottom-left{
                width: 65%;
                margin-left: auto;
                // border: 1px solid blueviolet;
                position: relative;
                overflow: hidden;
              }
              img{
                max-width: 80%;
                position: absolute;
                right: 0;
                bottom: 0;
                top: 20px;
                @media(min-width: 768px){
                  max-width: 100%;
                }
              }
            }
          }

          &:hover {
            -webkit-box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            -moz-box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            transform: scale(1.01);
            transition: all 0.3s ease-in-out;
            cursor: pointer;
          }
          
          &:nth-of-type(3),
          &:nth-of-type(4) {
            margin-top: 3%;
            @media (min-width: 1000px) {
              margin-top: 0;
            }
          }
        }
      }
    }
  }
}
//VU40001878
</style>