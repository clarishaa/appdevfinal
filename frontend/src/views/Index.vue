<template>
  <Carousel />
  <Feature />
  <Menus />
  <Facts />
  <Services />
  <Quote />
  <Team />
  <Testimonials />
</template>
  
<script>
// @ is an alias to /src
import Carousel from '@/components/User/Carousel.vue'
import Feature from '@/components/User/Feature.vue'
import About from '@/components/User/About.vue'
import Facts from '@/components/User/Facts.vue'
import Features2 from '@/components/User/Features2.vue'
import Services from '@/components/User/Services.vue'
import Quote from '@/components/User/Quote.vue'
import Menus from '@/components/User/Menus.vue'
import Team from '@/components/User/Team.vue'
import Testimonials from '@/components/User/Testimonials.vue'


export default {
  name: 'Index',
  components: {
    Carousel, Feature, About, Facts, Features2, Services, Quote, Menus, Team, Testimonials,
  },
  mounted() {

    this.loadScripts();

  },
  methods: {
    loadScripts() {
      const scriptUrls = [
        '/lib/jquery.min.js',
        '/lib/wow/wow.min.js',
        '/lib/easing/easing.min.js',
        '/lib/waypoints/waypoints.min.js',
        '/lib/owlcarousel/owl.carousel.min.js',
        '/lib/counterup/counterup.min.js',
        '/lib/parallax/parallax.min.js',
        '/lib/isotope/isotope.pkgd.min.js',
        '/lib/lightbox/js/lightbox.min.js',
        '/js/main.js',

      ];

      const head = document.getElementsByTagName('head')[0];

      function loadScript(index) {
        if (index < scriptUrls.length) {
          const script = document.createElement('script');
          script.src = scriptUrls[index];
          script.async = true;

          script.onload = function () {
            loadScript(index + 1);
          };

          head.appendChild(script);
        }
      }

      loadScript(0);
    },
  },
}
</script>
  