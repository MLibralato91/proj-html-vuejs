<template>
  <TitleSectionComponent :type="'Blog'" :titleBold="'Latest'" :title="'Posts'"
    :text="'When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.'" />

  <div class="row p-5">
    <CardPostsComponent :latest="true" :date="'April 21, 2023'" :name="'by Paul'"
      :title="'Clearing Corporations get SEBI nod to invest in overnight funds'"
      :text="'When, while the lovely valley teems with vapour around meand the meridian sun...'" />
    <CardPostsComponent :date="'April 21, 2023'" :name="'by Paul'"
      :title="'Clearing Corporations get SEBI nod to invest in overnight funds'"
      :text="'When, while the lovely valley teems with vapour around meand the meridian sun...'" />
    <CardPostsComponent :date="'April 21, 2023'" :name="'by Paul'"
      :title="'Clearing Corporations get SEBI nod to invest in overnight funds'"
      :text="'When, while the lovely valley teems with vapour around meand the meridian sun...'" />
  </div>
</template>

<script>
import TitleSectionComponent from './TitleSectionComponent.vue';
import CardPostsComponent from './CardPostsComponent.vue';
export default {
  name: 'LatestPostComponent',
  components: {
    TitleSectionComponent,
    CardPostsComponent
  }
}
</script>

<style lang="scss" scoped>
@media (max-width: 768px) {
  .row {
    display: flex;
    flex-direction: column;

  }
}
</style>