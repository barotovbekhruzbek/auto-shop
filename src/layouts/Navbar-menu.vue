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
</template>

<script>
export default {
  name: "Navbar-menu"
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
  .navbar-menu {
    height: auto;
    padding-bottom: 20px;
  }
  .menu-main ul {
    flex-direction: column;
    justify-content: center;
    text-align: center;
    gap: 10px;
  }
}
</style>