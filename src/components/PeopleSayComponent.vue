<template>
  <TitleSectionComponent :type="'Testimonials'" :titleBold="'What'" :title="'People Say'"
    :text="'When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.'" />
  <div class="row p-5">
    <CardPeopleComponent v-for="person in persons" :img="person.src" :name="person.name" />

  </div>
  <div class="row">
    <SponsorsComponent />
  </div>
</template>

<script>
import TitleSectionComponent from './TitleSectionComponent.vue';
import CardPeopleComponent from './CardPeopleComponent.vue';
import SponsorsComponent from './SponsorsComponent.vue';
import { people } from '../data/data'
export default {
  name: 'PeopleSayComponent',
  components: {
    TitleSectionComponent,
    CardPeopleComponent,
    SponsorsComponent
  },
  data() {
    return {
      persons: people
    }
  }
}
</script>

<style lang="scss" scoped></style>