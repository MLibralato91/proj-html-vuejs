<template>
  <div class="container py-5">
    <TitleSectionComponent :type="'Portfolio'" :titleBold="'Latest'" :title="'work'" />
  </div>
  <div class="carousel py-5">
    <div class="row w-100 m-0">

      <CardCarouselComponent v-for="work in allWorks" :img="work.src" :title="work.title" :role="work.role" />


    </div>
  </div>
</template>

<script>
import TitleSectionComponent from './TitleSectionComponent.vue';
import CardCarouselComponent from './CardCarouselComponent.vue'
import { works } from '../data/data';
export default {
  name: 'CarouselComponent',
  components: {
    TitleSectionComponent,
    CardCarouselComponent
  },
  data() {
    return {
      allWorks: works
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  text-align: center;

}
</style>