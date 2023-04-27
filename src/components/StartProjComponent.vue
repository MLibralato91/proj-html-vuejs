<template>
  <div class="row">
    <div class="left col-6 text-center">
      <img class="img-fluid" src="../../public/images/men-data.png" alt="">
    </div>

    <div class="right col-6 d-flex flex-column">
      <span class="small pb-3">Start Your Project</span>
      <h2 class="fw-bolder">Grow Your Business</h2>
      <h3>With Our Strategy</h3>
      <p class="small">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .of the
        impenetrable foliage of my trees, and but a few stray gleams steal into the inner sanctuary.</p>
      <div class="btnHome">
        <span class="btnPink me-3 small"><a href="#">Try it Now</a></span>
        <span class="btnBlue small"><a href="#">Explore More</a></span>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'StartProjComponent'
}
</script>

<style lang="scss" scoped>
.left{
  padding-top: 100px;
}

h2,
h3 {
  width: 70%;
  font-size: 3rem;
}

p {
  width: 70%;
  padding-top: 40px;
  padding-bottom: 50px;
}
img{
  width: 50%;
  
}
</style>