<template>
  <div class="d-flex flex-column page">
    <NavBar/>
    <div class="flex-shrink-1 main__container flex-grow-1">
      <div class="px-4">
        <div class="application__container guest__container">
          <div class="status__block d-flex flex-column align-center justify-center">
            <icon icon-name="success-payment"/>
            <p class="text-center mt-4">Оплата прошла успешно</p>
          </div>
          <div class="application__block">
            <img class="mr-5" src="../../assets/images/avatar.png" alt="">
            <div>
              <h4>Джалиль Мухамединов </h4>
              <p>ID: 1305304</p>
            </div>
          </div>
          <div class="application__block mt-5 d-block">
            <div class="d-flex align-center">
              <img class="mr-5" src="../../assets/images/restaurant-logo.png" alt="">
              <h4>Ресторан Дареджани</h4>
            </div>
            <v-divider class="my-4"/>
            <div class="app__row">
              <p>Счет</p>
              <p>4 990 ₸</p>
            </div>
            <div class="app__row">
              <p>Обслуживание (10%)</p>
              <p>499 ₸</p>
            </div>
            <div class="app__row">
              <p>Чаевые</p>
              <p>1 000 ₸</p>
            </div>
            <v-divider class="my-4"/>
            <div class="app__row">
              <p class="total">Общая сумма</p>
              <p class="font-weight-bold total">6 489 ₸</p>
            </div>
          </div>
          <v-btn class="mt-8 primary__btn" elevation="0">Вернуться на главную</v-btn>
        </div>
      </div>
    </div>
    <Footer/>
  </div>
</template>

<script setup>
import NavBar from '../../components/NavBar'
import Footer from "../../components/Footer";
import Icon from "../../components/icon";
</script>