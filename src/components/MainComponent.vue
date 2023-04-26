<template>
  <main>

    <section class="shots">
      <div class="container whatWeDo">
        whatWeDo
      </div>
    </section>
   
    <section class="even">
      <div class="container grow">
        grow
      </div>
    </section>
   
    <section class="shots">
      <div class="container works">
        works
      </div>
    </section>
    
    <section class="even">
        <div class="container ourPricing">
          ourPricing
        </div>
    </section>
    
    <section class="shots">
      <div class="container latestPost">
        latestPost
      </div>
      <div class="container whatPeopleSay">
        whatPeopleSay
      </div>
    </section>
  </main>
</template>

<script>
  export default {
    name: 'MainComponent'
  }
</script>

<style lang="scss" scoped>
.shots{
  width: 100%;
  height: 500px;
}

.even{
  width: 100%;
  height: 500px;
  background-image: linear-gradient(180deg, #08123d, #020332);
  color: white;
}
</style>