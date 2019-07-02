<template>
  <div id="homepage" class="center-xs">
    <Navigation></Navigation>
    <Hero></Hero>
    <Trustpilot></Trustpilot>
    <QuickLinks></QuickLinks>
    <BlueSection></BlueSection>
    <QuoteBenefits></QuoteBenefits>
    <Footer></Footer>
  </div>
</template>

<script>
import Navigation from './Navigation';
import Hero from './Hero';
import Trustpilot from './Trustpilot';
import QuickLinks from './QuickLinks';
import BlueSection from './BlueSection';
import QuoteBenefits from './QuoteBenefits';
import Footer from './Footer';

export default {
  /* eslint-disable */
  name: 'homepage',
  components: {
    Navigation,
    Hero,
    Trustpilot,
    QuickLinks,
    BlueSection,
    QuoteBenefits,
    Footer
  },
  data(){
    return {
      showNavbar: false
    }
  },
  methods:{
    handleScroll(e){
      window.pageYOffset > 50 ? 
        this.showNavbar = true :
        this.showNavbar = false;
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
  #homepage{
    position: relative;
  }
</style>
