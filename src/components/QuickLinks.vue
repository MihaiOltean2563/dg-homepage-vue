<template>
  <section id="quick-links">
    <div class="quick-links-wrapper center-xs">
      <div class="container">
        <h1 class="quick-links-greeting"><strong>Keep your home running smoothly</strong></h1>
        <div class="quick-links-wrapper between-sm">
          <div id="3576035" class="appliance" data-type="washing-machine">
            <a href="https://www.domesticandgeneral.com/goal-search/household-en/washing-machine-protection">
            </a>
          </div>
          <div id="8261695" class="appliance" data-type="dishwasher">
            <a href="https://www.domesticandgeneral.com/goal-search/household-en/dishwasher-protection">
            </a>
          </div>
          <div id="2688671" class="appliance" data-type="fridge-freezer">
            <a href="https://www.domesticandgeneral.com/goal-search/household-en/fridge-freezer-44">
            </a>
          </div>
          <div id="6165187" class="appliance" data-type="all-appliances">
            <a href="https://www.domesticandgeneral.com/products">
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  
}
</script>

<style lang="scss">
#quick-links{
  background: #eaeaea;
  
  .quick-links-wrapper{
    @media(min-width: 768px){
      display: flex;
    }
    .container{
      // border: 1px solid goldenrod;
      padding-bottom: 90px;

      .quick-links-greeting{
        font-size: 25px;
        line-height: 30px;
        color: #333333;
        padding: 90px 0;
        @media(min-width: 768px){
          font-size: 35px;
          line-height: 49px;
        }
        
      }
  
      .quick-links-wrapper{
        // border: 1px solid goldenrod;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
        padding: 0 20px;
        @media(min-width: 768px){
          padding: 0;
        }
        .appliance{
          height: 230px;
          background: #fff;
          box-shadow: 1px 1px 10px 1px #c0c1cc;
          -moz-box-shadow: 1px 1px 10px 1px #c0c1cc;
          -webkit-box-shadow: 1px 1px 10px 1px #c0c1cc;
          flex-basis: 45%;
          max-width: 45%;
          background: url('../assets/coming-soon.png');
          background-size: contain;
          background-repeat: no-repeat;
          transition: all .3s ease-in-out;

          &:hover{
            -webkit-box-shadow:0 0 10px rgba(0, 0, 0, 0.5);
            -moz-box-shadow:0 0 10px rgba(0, 0, 0, 0.5);
            box-shadow:0 0 10px rgba(0, 0, 0, 0.5);
            transform: scale(1.01);
            transition: all .3s ease-in-out;
            cursor: pointer;
          }
          @media(min-width: 768px){
            flex-basis: 23%;
            max-width: 23%;
            margin-top: 0; 
          }
          &:nth-of-type(3),
          &:nth-of-type(4){
            margin-top: 3%;
            @media(min-width: 768px){
              margin-top: 0;
            }
          }
        }
      }
    }
  }
}
</style>
