<template>
  <div class="col-lg-3 col-md-12 cardPost" :class="{ lastPost: latest }">
    <div class="post p-5 text-start" :class="{ lastBg: latest }">
      <div class="bodyPost">
        <p class="small">{{ date }} &middot; {{ name }}</p>
        <h5 class="fw-bolder">{{ title }}</h5>
        <p class="small">{{ text }}</p>
      </div>
      <div class="pt-4">
        <span class="btnWhite"><a href="#">Read More</a></span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardPostsComponent',
  props: ['date', 'title', 'text', 'name', 'latest']
}
</script>

<style lang="scss" scoped>
.btnWhite {
  padding: 10px 25px;
  border-radius: 20px;
  background-color: white;

  a {
    color: black;
  }
}

.post {
  background-image: linear-gradient(300deg, #122681, #020332);
  height: 400px;
  border-radius: 25px;
  color: white;

  p {
    padding-top: 20px;
  }
}

.lastBg {
  background-image: url(../../public/images/headway-537308-unsplash-1380x703.jpg);
  filter: grayscale(50%);
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
  align-items: end;
  line-height: 1;
  text-align: end;

  .bodyPost {
    width: 70%;
  }
}

.lastPost {
  width: 50%;
}

@media (max-width: 768px) {

  .lastPost {
    width: 100%;
  }

  .bodyPost {
    width: 100%;
    align-items: center;
    text-align: center;
  }

  .lastBg {
    width: 100%;
  }

  .post {
    margin-top: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: auto;
  }
}
</style>