<template>
  <div class="col-lg-3 col-md-12">
    <div class="myCard p-5">
      <div class="myCardImg">
        <img :src="img" :alt="title" class="">
      </div>
      <div class="myCardBody pt-4">
        <h5 class="fw-bolder">{{ title }}</h5>
        <p class="small pt-3">{{ paragraph }}</p>
        <!-- <p class="small pt-3" :class="{ redTitle: red }">{{ paragraph }}</p> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'WhatWeDoComponent',
  props: ['img', 'title', 'paragraph', 'red']

}
</script>

<style lang="scss" scoped>
.myCardImg {
  width: 120px;
  height: 120px;
  margin-left: auto;
  margin-right: auto;

}

img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.redTitle {
  color: red;
}
</style>