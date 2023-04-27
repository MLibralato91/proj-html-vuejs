<template>
  <div class="myCard" :class="{ active: isActive }">
    <h3 class="fw-bolder">{{ title }}</h3>
    <sub class="text-uppercase">{{ category }}</sub>
    <h3 class="num fw-bolder">
      <p class="">$</p>
      {{ price }}
    </h3>
    <sub>Per Month</sub>
    <ul class="small py-5">
      <li><span class="fw-bolder">Creative </span>Design Enabled</li>
      <li><span class="fw-bolder">Vibrant </span>Color Usage</li>
      <li><span class="fw-bolder">Eye </span>Catching Design</li>
      <li><span class="fw-bolder">Extreme </span>Typography</li>
      <li><span class="fw-bolder">Exceptional </span>Design</li>
    </ul>
    <span class="btnPink" :class="{btnActive: btnIsActive}"><a href="#">Order Now</a></span>

  </div>
</template>

<script>
export default {
  name: 'CardPriceComponent',
  props: ['title', 'price', 'category', 'isActive', 'btnIsActive']
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables.scss' as *;

.num {
  font-size: 5rem;
  padding-top: 50px;
  position: relative;
}

ul {
  span {
    margin-left: auto;
    margin-right: auto;

  }
  li{
    line-height: 2.5;
    font-size: 0.7rem;
  }
}

.myCard {
  background-color: white;
  color: black;
  border-radius: 20px;
  padding: 30px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.active{
  background: linear-gradient(180deg, $darkpink-btn, $lightpink-btn);
  color: white;

}
.btnActive{
  background-color: white;
  color: $pink-text;
}
p {
  font-size: 0.7rem;
  position: absolute;
  left: 70px;
  top: 30px;
}

h3 {
  line-height: 0.5;
  padding-top: 25px;
}</style>