<template>
  <header>

    <div class="container">
      <div class="topHeader d-flex justify-content-between align-items-center">
        <div class="logo">
          <img src="../../public/images/white-logo-2.png" alt="">
        </div>
        <div class="navlinks w-50">
          <ul class="d-flex justify-content-between align-items-center small">
            <li v-for="link in navLink">
              <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
            </li>
            <span class="btnBlue small "><a class="text-white" href="#">Sign in</a></span>
          </ul>
        </div>
      </div>
      <div class="mainHeader">
        <div class="row">
          <div class="left col-6 d-flex flex-column">
            <h2 class="fw-bolder">Business Planning</h2>
            <h3>Digital Technology</h3>
            <h2 class="fw-bolder">Modern Solution !</h2>
            <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .
            </p>
            <div class="btnHome">
              <span class="btnPink me-3 small"><a href="#">Try it Now</a></span>
              <span class="btnBlue small"><a href="#">Explore More</a></span>

            </div>
          </div>
          <div class="right col-6">
            <img class="img-fluid" src="../../public/images/header.png" alt="">

          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import { navLinks } from '../data/data'
export default {
  name: 'HeaderComponent',
  data() {
    return {
      navLink: navLinks
    }
  }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables.scss' as *;

header {
  width: 100%;
  background-image: linear-gradient(180deg, #0c1a58, #020332);
  color: white;
}

.topHeader {
  height: 80px;
}

.left {
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

.container {
  padding-bottom: 100px;
}

.active {
  color: $pink-text;
}

.navlinks a:hover {
  color: $pink-text;
}


</style>