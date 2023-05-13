<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Navbar from "../src/layouts/Navbar.vue"
import NavbarMenu from "./layouts/Navbar-menu.vue";
</script>

<template>
  <header>

    <div>
      <Navbar />
      <NavbarMenu />
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
