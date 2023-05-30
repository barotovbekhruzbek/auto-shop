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

  @media (max-width:900px) {
    .container {
      max-width: 800px;
    }
  }
  
  @media (max-width:600px) {
    .container {
      max-width: 500px;
    }
  }
  @media (max-width:450px) {
    .container {
      max-width: 400px;
    }
  }
</style>