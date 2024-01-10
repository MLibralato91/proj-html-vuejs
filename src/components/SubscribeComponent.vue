<template>
  <div class="boxSubscribe text-start d-flex justify-content-between align-items-center">
    <div class="text w-50">
      <h2 class="fw-bolder">We Offer Awesome Services</h2>
      <p class="small">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper
        surface.</p>
    </div>
    <div class="inputSubscribe">
      <input type="text">
      <span><a href="">Subscribe</a></span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SubscribeComponent'
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables.scss' as *;

.boxSubscribe {
  background: linear-gradient(90deg, $darkpink-btn, $lightpink-btn);
  padding: 50px;
  border-radius: 40px;
  height: 200px;
  color: white;
}

.inputSubscribe {

  input {
    width: 400px;
    height: 50px;
    padding-right: 50px;
    border-start-end-radius: 25px;
    border-end-end-radius: 25px;
    border-start-start-radius: 25px;
    border-end-start-radius: 25px;
    border-style: none;
  }

  span {
    margin-left: -125px;
    height: 20px;
    width: 50px;
    padding: 10px 25px;
    border-radius: 20px;
    background: linear-gradient(90deg, $lightblue-btn, $darkblue-btn);
  }
}

@media (max-width:768px) {
  .boxSubscribe {
    flex-direction: column;
    padding: 20px 50px;

    .text {
      width: 100% !important;
    }
  }
}
</style>