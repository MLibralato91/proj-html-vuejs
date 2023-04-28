<template>
  <TitleSectionComponent :type="'Testimonials'" :titleBold="'What'" :title="'People Say'"
    :text="'When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.'" />
  <div class="row p-5">
    <CardPeopleComponent :img="'../../public/images/philipe-cavalcante-539505-unsplash-1024x1024.png'"/>
    <CardPeopleComponent :img="'../../public/images/fabio-spinelli-695744-unsplash-1024x1024.png'"/>
    <CardPeopleComponent :img="'../../public/images/szabo-viktor-1266895-unsplash-1024x1024.png'"/>
  </div>

</template>

<script>
import TitleSectionComponent from './TitleSectionComponent.vue';
import CardPeopleComponent from './CardPeopleComponent.vue';
export default {
  name: 'PeopleSayComponent',
  components: {
    TitleSectionComponent,
    CardPeopleComponent
  }
}
</script>

<style lang="scss" scoped></style>