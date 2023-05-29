<template>
  <div class="container">
    <BannerVue />
    <Category />
  </div>
</template>

<script>
import BannerVue from './components/Banner.vue'
import Category from './components/Category.vue';

export default {
    components: {
    BannerVue,
    Category
}
}
</script>

<style scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
  .container {
    max-width: 1200px;
    margin: 0 auto;
  }
</style>