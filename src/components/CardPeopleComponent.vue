<template>
<div class="col-4 text-center">
    <img :src="img" :alt="name">
    <div class="stars small py-5">
      <i class="fa-solid fa-star"></i>
      <i class="fa-solid fa-star"></i>
      <i class="fa-solid fa-star"></i>
      <i class="fa-regular fa-star"></i>
      <i class="fa-regular fa-star"></i>
    </div>
    <div class="text">
      <p class="small">When, while lovely valley teems with vapour around meand meridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.</p>
    </div>
    <div class="user">
      <h6 class="fw-bolder">{{name}}</h6>
      <p class="small">Marketing Management</p>
    </div>
</div>
</template>

<script>
  export default {
    name:'CardPeopleComponent',
    props:['img', 'name']
  }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables.scss' as *;
.stars i{
  color:$pink-text ;
}
img{
  width: 100px;
  border-radius: 50%;
  border: 4px solid $pink-text;
}
</style>