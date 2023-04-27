<template>
  <div class="col-3">
    <div class="myCard p-5">
      <div class="myCardImg">
        <img :src="img" :alt="title" class="">
      </div>
      <div class="myCardBody pt-4">
        <h5 class="fw-bolder">{{ title }}</h5>
        <p class="small pt-3">{{ paragraph }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'WhatWeDoComponent',
  props: ['img', 'title', 'paragraph']

}
</script>

<style lang="scss" scoped>
.myCardImg{
  width: 120px;
  height: 120px;
  margin-left: auto;
  margin-right: auto;
  
}
img{
  width: 100%;
  height: 100%;
  object-fit: contain;
}
</style>