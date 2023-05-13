<template>
  <div class="navbar-menu">
      <div class="container">
          <div class="menu-main">
            <ul>
              <li><a href="#">Каталог </a></li>
              <li><a href="#">О магазине </a></li>
              <li><a href="#">Доставка </a></li>
              <li><a href="#"> Оплата</a></li>
              <li><a href="#"> Гарантия</a></li>
              <li><a href="#"> Контакты</a></li>
            </ul>
          </div>
      </div>



  </div>
  <button @click="showMenu = !showMenu" class="burger-menu">
    <i class="fas fa-bars"></i>
  </button>

  <div class="menu" :class="{ 'menu-open': showMenu }">
    <div class="menu-link">
      <ul>
        <li><a href="#">Каталог </a></li>
        <li><a href="#">О магазине </a></li>
        <li><a href="#">Доставка </a></li>
        <li><a href="#"> Оплата</a></li>
        <li><a href="#"> Гарантия</a></li>
        <li><a href="#"> Контакты</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar-menu",
  data () {
    return {
      showMenu: false,

    }
  }
}
</script>

<style scoped>
.navbar-menu {
  width: 100%;
  height: 60px;
  background-color: #0A67CB;
}
.container {
  max-width: 1200px;
  margin: 0 auto;
}
.menu-main ul {
  padding-top: 20px;
  display: flex;
  list-style: none;
  justify-content: space-between;
}
.menu-main ul li a {
  text-decoration: none;
  color: white;
  font-weight: 700;
  font-size: 14.82px;
}
/* mobile menu*/


.burger-menu {
  background: none;
  border: none;
  cursor: pointer;
  display: none;
}

.burger-menu i {
  font-size: 25px;
}
.menu {
  position: fixed;
  top: 0;
  left: -250px;
  width: 250px;
  height: 100%;
  background-color: #0A67CB;
  transition: all 0.3s ease-in-out;
}
.menu ul{
  display: flex;
  flex-direction: column;
  justify-content: center;
  list-style: none;
  gap: 15px;
}
.menu ul li a {
  text-decoration: none;
  color: white;
  font-size: 22px;
}
.menu-open {
  left: 0;
}


@media (max-width: 900px) {
  .container {
    max-width: 900px;
  }
  .menu-main ul {
    justify-content: space-around;
  }
}

@media (max-width: 600px) {
  .container {
    max-width: 550px;
  }
  .burger-menu {
    display: block;
  }
  .navbar-menu {
   display: none;
  }

}
</style>



