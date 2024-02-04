<template>
  <div id="app">
    <header class="header">
      <div class="container header_container">
        <div class="burger">
          <img src="./assets/бургер.svg" alt="Menu">
        </div>
        <div class="logo">
          <img src="./assets/лого.svg" alt="Logo">
        </div>
        <nav class="navigation">
          <ul class="navigation_list">
            <li> <a class="link" href="">О нас</a>  </li>
            <li> <a class="link" href="">Доставка и оплата</a>  </li>
            <li> <a class="link" href="">Регистрация продукта</a>  </li>
            <li> <a class="link" href="">Сервис</a>  </li>
            <li> <a class="link" href="">Сертификаты и лицензии</a>  </li>
          </ul>
        </nav>
        <div class="personal">
          <div class="basket">
            <img src="./assets/basker.svg" alt="Basket">
          </div>
        </div>
      </div>
    </header>
    <section class="main">
      <div class="container main_container">
        <div class="main_left">
          <h1 class="main_title">Уникальные технологии для ухода за волосами</h1>
          <p class="main_description">Идеальная укладка для всех типов волос вместе с Dyson</p>
          <button class="main_button">
            <p class="main_button_text">Подробнее</p>
          </button> 
            
        </div>
        <div class="main_right">
          <img class="main_image" src="./assets/girl1.png" alt="girl">
        </div>
      </div>
    </section>
    <section class="offers">
      <div class="container offers_container">
        <ul class="offers_list">
          <li class="offers_item" v-for="(_,index) in 8" :key="index">
            <offer-card-component />
          </li>
        </ul>
      </div>
    </section>
    <section class="about">
      <div class="container about_container">
        <div class="about_left">
          <h3 class="about_left_title">Мнение экспертов о технике Dyson</h3>
          <p class="about_left_description">
            Сегодня многие стилисты и салоны красоты в своей работе используют технику от Dyson. <br><br>

Несмотря на высокую стоимость, техника Dyson помогает экономить. Мастера тратят меньше времени на сушку и укладку волос, благодаря чему успевают обслужить большее количество клиентов. Также устройства  от Dyson потребляют значительно меньше электроэнергии, не теряя свою мощность.<br> <br>

Фены Dyson универсальны. Они подходят для сушки разных типов волос. Насадки из комплекта помогают создавать укладки на любой вкус. Функциональность девайсов впечатляет не меньше, чем их уникальный дизайн. <br><br>

Ведущие стилисты отмечают, что техника Dyson для ухода за волосами идеально подходят для длительной работы за счет своей эргономичности. А за счет бесшумности инновационного мотора использование устройств стало максимально комфортным. <br><br>

          </p>
        </div>
        <div class="about_right">
          <img src="./assets/girl3.png" alt="girl">
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import OfferCard from "./components/Cards/OfferCard.vue"

export default {
  name: 'App',
  components: {
    "offer-card-component": OfferCard
  }
  


}
</script>

<style>

h1,h2,h3,h4,h5,h6 {
  margin: 0;
  padding: 0;
}

button {
  border: none;
  outline: none;
  padding: 0;
}

ul {
  padding: 0;
  list-style: none;
}

body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}




.container {
  width: 100%;
  max-width: 1360px;
  margin: 0 auto;
  padding-left: 40px;
  padding-right: 40px;
}


.header {
  height: 90px;
  background: #111111;
}

.header_container {
  display: flex;
  height: 90px;
  align-items: center;
}




.burger {
  margin-right: 50px;
}
.logo {
  margin-right: 50px;
}
.navigation {
  margin-right: 60px;
}
.navigation_list{
  margin: 0;
  padding: 0;
  display: flex;
  column-gap: 30px;
  list-style: none;
  color: white;
}

.link {
  color: white;
  text-decoration: none;
  font-weight: 400;
  font-size: 20px;
}

.personal {
  margin-left: auto;
}

.main {
  width: 100%;
  height: 850px;
  background-color: #ddd;
  overflow: hidden;
  
}
.main_container{
  display: flex;
  align-items: center;
  position: relative;
  height: 100%;
}

.main_left{
  max-width: 556px;
  font-weight: bold;
  z-index: 1;
}

.main_right{
  position: absolute;
  top: 0;
  bottom: 0;
  right: -220px;
  z-index: 0;
}

.main_image{
  width: 100%;
  height: 100%;
  object-fit: contain;
}


.main_title{ 
  font-weight: 400;
  font-size: 46px;
  color: #111;
  margin-bottom: 40px;
}
.main_description{
  
  font-weight: 200;
  font-size: 26px;
  color: #111;
  margin-bottom: 90px;
}
.main_button{
  border-radius: 3px;
  padding: auto;
  width: 235px;
  height: 64px;
  background: #c5358c;  
}

.main_button_text{
  
  font-weight: 400;
  font-size: 19px;
  text-align: center;
  color: #fff;
}

.offers_list{
  display: grid;
  grid-template-columns: repeat(4,1fr);
  gap: 20px;
}

.offers_container {
  padding-top: 150px;
  padding-bottom: 150px;
}

.about {
  background-color : #f8f8f8;  
}

.about_container{
  display: flex;
  align-items: center;
  position: relative;
  height: 100%;
}


.about_left{
  max-width: 580px;
    font-weight: bold;
    z-index: 1;
}
.about_left_title{
  font-weight: 400;
  font-size: 35px;
  color: #111;
}
.about_right{
  top: 0;
  bottom: 0;
  right: -220px;
  z-index: 0;
}


</style>
