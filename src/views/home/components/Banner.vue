<template>
  <div class="banner">
    <div class="banner-wrapper">
      <div class="banner-left">
        <div class="banner-left-title">
          <p>Каталог легковых запчастей</p>
          <h3>Для иномарок и <br>
            отечественных авто</h3>
        <p>Более 7 000 наименований</p>
        <button>Смотреть каталог</button>
        </div>
      </div>
      <div class="banner-right">
       <div class="banner-right-wrapper">
        <div class="banner-box box-1">
          <p>Масла и автохимия</p>
        </div>
        <div class="banner-box box-1">
          <p>Масла и автохимия</p>
        </div>
       </div>
       <div class="banner-right-wrapper">
        <div class="banner-box box-1">
          <p>Масла и автохимия</p>
        </div>
        <div class="banner-box box-1">
          <p>Масла и автохимия</p>
        </div>
       </div>
      
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style  scoped>
.banner {
  margin-top: 30px;
}
.banner-wrapper {
  display: flex;
  gap: 10px;
 
}
  .banner-left {
    width: 760px;
    background: url("../../../images/banner-left.png");
    background-repeat: no-repeat;
    height: 430px;
   
  }
  .banner-left-title {
      color: white;
      padding: 3rem;
  }
  .banner-left-title p {
    font-weight: 600;
  font-size: 13px;
  line-height: 20px;
  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25), 0px 4px 4px rgba(0, 0, 0, 0.25);
  padding-top: 20px;
  }
  .banner-left-title h3 {
    padding: 10px 0;
    font-weight: 700;
    font-size: 35px;
    line-height: 38px;
    height: 76px;
  }

  .banner-left-title button {
    width: 260px;
    height: 50px;
    color: white;
    background: #0A67CB;
    border: 1px solid #0A67CB;
    margin-top: 30px;
  }
  .banner-right {
    /* display: flex; */
    gap: 10px;
  }
  .banner-right-wrapper {
    display: flex;
    gap: 10px;
  }
  .box-1 {
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    background: url("../../../images/banner-right.png");
    width: 210px;
    height: 210px;
  }

  .box-1 p {
    color: white;
    font-weight: 700;
    font-size: 18px;
    line-height: 28px;
    align-self: flex-end;
    padding-left: 20px;
    padding-bottom: 20px;
  }

  @media (max-width:900px) {
    .banner-wrapper {
    flex-wrap: wrap;
    justify-content: center;
 
}

@media (max-width: 600px) {
  .banner-left { 
    width: 100%;
  }
  .banner-right { 
    display: none;
  }
}
@media (max-width: 450px) {
  .banner-left { 
    width: 100%;
  }
  .banner-right { 
    display: none;
  }
  .banner-left-title h3 {
  
    font-size: 22px;
    line-height: 30px;
    height: auto;

  }
}
  }
</style>