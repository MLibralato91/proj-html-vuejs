<template>
  <main>

    <section class="shots">
      <div class="container whatWeDo text-center py-5">
        <p class="text-pink small">Our Services</p>
        <h2><span class="fw-bolder">What</span> We Do</h2>
        <p class="small pt-2">When, while the lovely valley teems with vapour around meand the</p>
        <div class="row py-5">
          <WhatWeDoComponent v-for="service in allService" :img="service.src" :title="service.title" :paragraph="service.text"/>
        </div>
        <span class="btnPink small"><a href="#">View All Services</a></span>
      </div>

    </section>

    <section class="even">
      <div class="container grow">
        <StartProjComponent/>
      </div>
    </section>

    <section class="shots">
      <div class="container works">
        works
      </div>
    </section>

    <section class="even">
      <div class="container ourPricing">
        ourPricing
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
import { services } from '../data/data'
export default {
  name: 'MainComponent',
  components: {
    WhatWeDoComponent,
    StartProjComponent
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

.grow{
  padding: 100px 0 100px 0;
}
</style>