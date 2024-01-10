<template>
  <div class="col-lg-3 col-md-12 ">
    <div class="cardCarousel">
      <div class="boxImg">
        <img :src="img" :alt="title">
      </div>
      <div class="title d-flex justify-content-between small">
        <h6 class="fw-bolder">{{ title }}</h6>
        <p>{{ role }}</p>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'CardCarouselComponent',
  props: ['img', 'title', 'role']
}
</script>

<style lang="scss" scoped>
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 20px;
}

.cardCarousel {
  border-radius: 20px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

.title {
  padding: 20px;
  padding-top: 30px;
}

@media (max-width:768px) {
  .cardCarousel {
    margin-top: 20px;

  }
}
</style>