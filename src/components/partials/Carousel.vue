<template>
  <v-carousel 
    cycle
    id="carousel"
    show-arrows-on-hover
    >
      <v-carousel-item 
        v-for="(slide, i) in slides" 
        :key="i"
      >
         <iframe id="frame" :src="slide.src"  width="100%" height="500">
           <v-img contain :src="slide.src" height="90%" width="90%"></v-img>
         </iframe>

        <!-- <v-row
          align="center"
          justify="center"
        >
          <v-col class="text-center" cols="12">
            <h1 class="display-1 font-weight-thin mb-4">Vuetify.js</h1>
            <h4 class="subheading">Build your application today!</h4>
          </v-col>
        </v-row> -->
      </v-carousel-item>
  </v-carousel>
</template>



<script>
  export default {
    data () {
      return {
        slides: [
          
          {
            src: 'https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/finance_0bdk.svg',
          },
          {
            src: 'https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/investing_7u74.svg',
          },
          {
            src: 'https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/personal_finance_tqcd.svg',
          },
          {
            src: 'https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/around_the_world_v9nu.svg',
          },
          {
            src: 'https://42f2671d685f51e10fc6-b9fcecea3e50b3b59bdc28dead054ebc.ssl.cf5.rackcdn.com/illustrations/business_deal_cpi9.svg',
          },
        ],
      }
    },
  }
</script>

<style scoped>
  #carousel {
    height: 500px !important;
  }

  #frame {
    border: none;
  }
</style>
