<template>
<div class="topPricing pt-5">
  <p class="text-pink small">Price List</p>
  <h2><span class="fw-bolder">Our</span> Pricing</h2>
  <p class="small">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .</p>
</div>
<div class="row">
  <div class="col-4">
    <CardPriceComponent :price="'40'" :title="'Designing'" :category="'process'"/>
  </div>
  <div class="col-4">
    <CardPriceComponent :price="'60'" :title="'Developing'" :category="'product'" :isActive="true" :btnIsActive="true"/>
  </div>
  <div class="col-4">
    <CardPriceComponent :price="'80'" :title="'Supporting'" :category="'clients'"/>
  </div>
  
</div>
</template>

<script>
import CardPriceComponent from './CardPriceComponent.vue';
  export default {
    name: 'PricingComponent',
    components:{
      CardPriceComponent
    }
  }
</script>

<style lang="scss" scoped>
.row{
  padding: 50px 150px;
}
</style>