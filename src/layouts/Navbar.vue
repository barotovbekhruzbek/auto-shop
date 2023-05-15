<template>
   <div class="navbar" v-bind:class="{backdrop: !showModal}">
        <div class="container">
            <div class="navbar-top">
                <div class="logo">
                    <img src="../../src/images/logo.png" alt="">
                </div>
                <div class="contact-navbar">
                    <i class="fas fa-phone"></i>
                    <span>8 800 550-58-19</span>
                    <p   @click="showModal = !showModal">Заказать звонок</p>
                </div>
            </div>
        </div>
        <transition name="appear">
		<div class="simple-modal" v-if="!showModal">
			<h1>Заказать звонок</h1>
			
                <div class="login-box">
  
  <form>
    <div class="user-box">
      <input type="text" name="" required="">
      <label>Ваше имя</label>
    </div>
    <div class="user-box">
      <input type="number" name="" required="">
      <label>Телефон</label>
    </div>
    <a href="#">
      <span></span>
      <span></span>
      <span></span>
      <span></span>
      отправлять
    </a>
  </form>
</div>
            
			<button class="btn-close" type="button" @click="showModal = !showModal">{{closeModal}}</button>
		</div>
	</transition>
   </div> 
</template>

<style scoped> 

    .navbar {
      width: 100%;
    }
    .container {
        max-width: 1200px;
        margin: 0 auto;
    }
    .navbar-top {
        padding-top: 10px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .contact-navbar i{
        color: #B2B2B2;
        font-size: 20px;
    }
    .contact-navbar span {
        padding-left: 8px;
        color: #000000;
        font-weight: 700;
        font-size: 17px;
        line-height: 26px;
    }
    .contact-navbar p {
        color: #0A67CB;
        font-size: 13.91px;
    }

    .simple-modal {
  width: 60vw;
  height: 70vh;
  box-shadow: 1px 1px 2px 0 rgba(0, 0, 0, 0.19);
  position: fixed;
  right: 15%;
  top: 15%;
  background: white;
  border-radius: 3px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2% 5%;
  z-index: 1;
  
}

@media (max-width:600px) {
  .simple-modal {
    top: 25%;
  }
  .simple-modal h1 {
    font-size: 22px;
  }
  .simple-modal .login-box {
    width: auto;
  }
}
.simple-modal p {
  text-align: center;
}
.simple-modal button {
  position: absolute;
  right: 10px;
  bottom: 10px;
  border-color: transparent;
}

.backdrop:after {
  content: "";
  width: 100%;
  height: 100%;
  background: black;
  position: absolute;
  -webkit-animation: backdrop 600ms ease forwards;
          animation: backdrop 600ms ease forwards;
}

@-webkit-keyframes backdrop {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 0.5;
  }
}

@keyframes backdrop {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 0.5;
  }
}
.appear-enter-active {
  -webkit-animation: appear 700ms ease;
          animation: appear 700ms ease;
}

.appear-leave-active {
  animation: appear 300ms ease reverse;
}

@-webkit-keyframes appear {
  0% {
    top: -100%;
  }
  2% {
    height: 102%;
  }
  5% {
    height: 115%;
  }
  10% {
    height: 120%;
  }
  20% {
    height: 125%;
  }
  100% {
    top: 10%;
  }
}

@keyframes appear {
  0% {
    top: -100%;
  }
  2% {
    height: 102%;
  }
  5% {
    height: 115%;
  }
  10% {
    height: 120%;
  }
  20% {
    height: 125%;
  }
  100% {
    top: 10%;
  }
}

/* form */

.login-box {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 400px;
  padding: 40px;
  transform: translate(-50%, -50%);
 

}



.login-box .user-box {
  position: relative;
}

.login-box .user-box input {
  width: 100%;
  padding: 10px 0;
  font-size: 16px;
  color: #000;
  margin-bottom: 30px;
  border: none;
  border-bottom: 1px solid #0A67CB;
  outline: none;
  background: transparent;
}
.login-box .user-box label {
  position: absolute;
  top:0;
  left: 0;
  padding: 10px 0;
  font-size: 16px;
  color: #000;
  pointer-events: none;
  transition: .5s;
}

.login-box .user-box input:focus ~ label,
.login-box .user-box input:valid ~ label {
  top: -20px;
  left: 0;
  color: #0A67CB;
  font-size: 12px;
}

.login-box form a {
  position: relative;
  display: inline-block;
  padding: 10px 20px;
  color: #0A67CB;
  font-size: 16px;
  text-decoration: none;
  text-transform: uppercase;
  overflow: hidden;
  transition: .5s;
  margin-top: 40px;
  letter-spacing: 4px
}

.login-box a:hover {
  background: #0A67CB;
  color: #fff;
  border-radius: 5px;
  box-shadow: 0 0 5px #0A67CB,
              0 0 25px #0A67CB,
              0 0 50px #0A67CB,
              0 0 100px #0A67CB;
}

.login-box a span {
  position: absolute;
  display: block;
}

.login-box a span:nth-child(1) {
  top: 0;
  left: -100%;
  width: 100%;
  height: 2px;
  background: linear-gradient(90deg, transparent, #0A67CB);
  animation: btn-anim1 1s linear infinite;
}

@keyframes btn-anim1 {
  0% {
    left: -100%;
  }
  50%,100% {
    left: 100%;
  }
}

.login-box a span:nth-child(2) {
  top: -100%;
  right: 0;
  width: 2px;
  height: 100%;
  background: linear-gradient(180deg, transparent, #0A67CB);
  animation: btn-anim2 1s linear infinite;
  animation-delay: .25s
}

@keyframes btn-anim2 {
  0% {
    top: -100%;
  }
  50%,100% {
    top: 100%;
  }
}

.login-box a span:nth-child(3) {
  bottom: 0;
  right: -100%;
  width: 100%;
  height: 2px;
  background: linear-gradient(270deg, transparent, #0A67CB);
  animation: btn-anim3 1s linear infinite;
  animation-delay: .5s
}

@keyframes btn-anim3 {
  0% {
    right: -100%;
  }
  50%,100% {
    right: 100%;
  }
}

.login-box a span:nth-child(4) {
  bottom: -100%;
  left: 0;
  width: 2px;
  height: 100%;
  background: linear-gradient(360deg, transparent, #0A67CB);
  animation: btn-anim4 1s linear infinite;
  animation-delay: .75s
}

@keyframes btn-anim4 {
  0% {
    bottom: -100%;
  }
  50%,100% {
    bottom: 100%;
  }
}
.btn-close {
    padding: 8px 40px;
    border: none;
    background-color: #0A67CB;
    color: white;
    border-radius: 10px;
}


@media (max-width: 1200px) {
    .container {
      max-width: 900px;
    }
  .navbar-top {
    justify-content: space-around;
  }

}
    @media (max-width: 600px) {
      .container {
        max-width: 550px;
      }
      .navbar-top {
        flex-direction: column;
        justify-content: center;
      }
    }
</style>

<script>
export default {
    data() {
        return {
            openModal: 'Click',
		    showModal: 'false',
		    closeModal: 'Закрить',
        }
    }
}
</script>