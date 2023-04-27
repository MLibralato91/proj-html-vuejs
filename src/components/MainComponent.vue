<template>
  <main>

    <section class="shots">
      <div class="container whatWeDo text-center py-5">
        <TitleSectionComponent :type="'Our Services'" :titleBold="'What'" :title="'We Do'"
          :text="'When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.'" />

        <div class="row py-5">
          <WhatWeDoComponent v-for="service in allService" :img="service.src" :title="service.title"
            :paragraph="service.text" />

          <!-- <WhatWeDoComponent  :title="'hello'" :paragraph="'luxastra'" :red="true"/> -->
        </div>
        <span class="btnPink small"><a href="#">View All Services</a></span>
      </div>

    </section>

    <section class="even">
      <div class="container grow">
        <StartProjComponent />
      </div>
    </section>

    <section class="shots">
      <div class="container works">
        Works
      </div>
    </section>

    <section class="even">
      <div class="container ourPricing text-center">
        <PricingComponent />
      </div>
    </section>

    <section class="shots">
      <div class="container latestPost">
        latestPost
      </div>
      <div class="container whatPeopleSay">
        whatPeopleSay
      </div>
    </section>
  </main>
</template>

<script>
import WhatWeDoComponent from './WhatWeDoComponent.vue';
import StartProjComponent from './StartProjComponent.vue'
import WorksComponent from './WorksComponent.vue';
import PricingComponent from './PricingComponent.vue';
import TitleSectionComponent from './TitleSectionComponent.vue';
import { services } from '../data/data'
export default {
  name: 'MainComponent',
  components: {
    WhatWeDoComponent,
    StartProjComponent,
    WorksComponent,
    PricingComponent,
    TitleSectionComponent
  },
  data() {
    return {
      allService: services,

    }
  }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables.scss' as *;

.shots {
  width: 100%;

}

.even {
  width: 100%;
  background-image: linear-gradient(180deg, #08123d, #020332);
  color: white;
}

.grow {
  padding: 100px 0 100px 0;
}

.ourPricing {
  height: 500px;
}

.latestPost {
  text-align: center;
  padding-top: 400px;
}</style>