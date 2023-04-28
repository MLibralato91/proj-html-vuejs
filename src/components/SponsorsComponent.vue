<template>
  <div class="col-12">
    <div class="sponsor d-flex justify-content-evenly align-items-center py-5">
      <div class="boxImg">
        <img src="../../public/images/client-1-1.png" alt="client-1-1">

      </div>
      <div class="boxImg">
        <img src="../../public/images/clienty-2.png" alt="clienty-2">

      </div>
      <div class="boxImg">
        <img src="../../public/images/clienty-3.png" alt="clienty-3">

      </div>
      <div class="boxImg">
        <img src="../../public/images/clienty-4.png" alt="clienty-4">

      </div>
      <div class="boxImg">
        <img src="../../public/images/client-5.png" alt="client-5">

      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name:'SponsorsComponent'
  }
</script>

<style lang="scss" scoped>
.boxImg{
  width: 80px;
  height: 40px;
}
img{
  width: 100%;
  height: 100%;
  object-fit: contain;
}
</style>