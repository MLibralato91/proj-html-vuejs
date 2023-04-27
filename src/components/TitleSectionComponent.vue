<template>
  <p class="text-pink small">{{ type }}</p>
  <h2><span class="fw-bolder">{{ titleBold }}</span> {{title}}</h2>
  <p class="small">{{text}}</p>
</template>

<script>
  export default {
    name: 'TitleSectionComponent',
    props: ['titleBold','title', 'type', 'text']
  }
</script>

<style lang="scss" scoped>

</style>