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
          <div class="left col-lg-6 col-md-12 d-flex flex-column">
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
          <div class="right col-lg-6 col-md-12">
            <transition
            appear
            @before-enter="beforeEnter"
            @enter="enter">
              <img class="img-fluid" src="../../public/images/header.png" alt="">

            </transition>

          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import  gsap  from "gsap";
import { navLinks } from '../data/data'
export default {
  name: 'HeaderComponent',
  data() {
    return {
      navLink: navLinks,
    }
  },
  setup(){
    const beforeEnter = (el)=>{
      console.log('Before');
      el.style.transform = 'translateX(800px)'
      el.style.opacity = 0
    }
    const enter = (el)=>{
      console.log('Enter');
      gsap.to(el,{
        duration:5,
        x:0,
        opacity:1
      })
    }

    return { beforeEnter, enter}
  }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables.scss' as *;

header {
  width: 100%;
  background-image: linear-gradient(180deg, #0c1a58, #020332);
  color: white;

  .container {
    padding-bottom: 100px;

    .topHeader {
      height: 80px;

      .navlinks a:hover {
        color: $pink-text;
      }
    }

    .mainHeader {


      .left {
        padding-top: 100px;

        p {
          width: 70%;
          padding-top: 40px;
          padding-bottom: 50px;
        }

        h2,
        h3 {
          width: 70%;
          font-size: 3rem;
        }
      }
    }

    .active {
      color: $pink-text;
    }
  }
}

@media (max-width: 768px) {

  header {
    width: 100%;
    background-image: linear-gradient(180deg, #0c1a58, #020332);
    color: white;

    .container {
      .mainHeader {
        text-align: center;

        .row {
          display: flex;
          flex-direction: column-reverse;
        }

        .right {
          padding-top: 50px;

          img {
            width: 60%;
          }
        }

        .left {
          padding-top: 50px;

          p {
            width: 100%;
          }

          h2,
          h3 {
            width: 100%;
            font-size: 3rem;
          }
        }
      }

    }
  }

}</style>