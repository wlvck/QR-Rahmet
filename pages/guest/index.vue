<template>
  <div class="d-flex flex-column page">
    <NavBar/>
    <div class="flex-shrink-1 main__container flex-grow-1">
      <div class="px-4">
        <div class="application__container">
          <h1>Ресторан Дареджани</h1>
          <div class="application__block">
            <img class="mr-5" src="../../assets/images/avatar.png" alt="">
            <div>
              <h4>Джалиль Мухамединов </h4>
              <p>ID: 1305304</p>
            </div>
          </div>
          <h3>Чаевые официанту</h3>
          <v-text-field label="Введите сумму"/>
          <div class="fastFill mt-3 mb-6">
            <p class="pointer orange__hover">500 ₸</p>
            <p class="pointer orange__hover">1000 ₸</p>
            <p class="pointer orange__hover">2000 ₸</p>
            <p class="pointer orange__hover">5000 ₸</p>
          </div>
          <v-divider/>
          <h3>Вам понравилось?</h3>
          <div class="mb-6">
            <icon class="mr-5 pointer" icon-name="ev-star"/>
            <icon class="mr-5 pointer" icon-name="ev-star"/>
            <icon class="mr-5 pointer" icon-name="ev-star"/>
            <icon class="mr-5 pointer" icon-name="ev-star"/>
            <icon class="pointer" icon-name="ev-star"/>
          </div>
          <v-text-field label="Ваш отзыв"/>
          <v-divider class="my-6"/>
          <v-btn class="primary__btn desktop" elevation="0" @click="selectBank=true">Оплатить</v-btn>
          <div class="grid__btn">
            <p class="mb-3">Оплата</p>
            <div>
              <v-btn class="primary__btn" elevation="0" @click="selectBank=true">Картой</v-btn>
              <v-btn class="secondary__btn" elevation="0">Другое</v-btn>
            </div>
          </div>
          <div class="checkbox mt-6">
            <input class="pointer" id="agreement" type="checkbox">
            <label for="agreement">Я хочу компенсировать комиссию сервиса транзакций, чтобы покрыть издержки на перевод
              средств сотруднику</label>
          </div>
          <div class="checkbox mt-4">
            <input class="pointer" id="policy" type="checkbox">
            <label for="policy">Согласен с условиями <a href="#">Пользовательского соглашения</a>
              и <a href="#">Политикой обработки персональных данных</a></label>
          </div>
          <v-divider class="my-6"/>
          <div class="application__block flex-column">
            <h4 class="mb-4">Сотрудничаем с банками</h4>
            <div class="bank__grid">
              <div>
                <icon icon-name="kaspi"/>
                <label>Kaspi</label>
              </div>
              <div>
                <icon icon-name="halyk"/>
                <label>HalykBank</label>
              </div>
              <div>
                <icon icon-name="bcc"/>
                <label>bcc.kz</label>
              </div>
              <div>
                <icon icon-name="jusan"/>
                <label>Jusan</label>
              </div>
              <div>
                <icon icon-name="forte"/>
                <label>forte</label>
              </div>
              <div>
                <icon icon-name="other-banks"/>
                <label>Другие банки</label>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer/>
    <v-dialog v-model="selectBank" width="456">
      <div class="modal__container">
        <div class="d-flex justify-end">
          <icon @click="selectBank = false" class="pointer" icon-name="close"/>
        </div>
        <div class="modal__title">
          Выберите банк
        </div>
        <div class="modal__row">
          <div class="pointer">
            <icon icon-name="kaspi"/>
            <label class="flex-shrink-1 flex-grow-1">Kaspi</label>
            <icon icon-name="arrow-right"/>
          </div>
          <div class="pointer">
            <icon icon-name="halyk"/>
            <label class="flex-shrink-1 flex-grow-1">HalykBank</label>
            <icon icon-name="arrow-right"/>
          </div>
          <div class="pointer">
            <icon icon-name="bcc"/>
            <label class="flex-shrink-1 flex-grow-1">bcc.kz</label>
            <icon icon-name="arrow-right"/>
          </div>
          <div class="pointer">
            <icon icon-name="jusan"/>
            <label class="flex-shrink-1 flex-grow-1">Jusan</label>
            <icon icon-name="arrow-right"/>
          </div>
          <div class="pointer">
            <icon icon-name="forte"/>
            <label class="flex-shrink-1 flex-grow-1">forte</label>
            <icon icon-name="arrow-right"/>
          </div>
          <div class="pointer">
            <icon icon-name="other-banks"/>
            <label class="flex-shrink-1 flex-grow-1">Другие банки</label>
            <icon icon-name="arrow-right"/>
          </div>
        </div>
      </div>
    </v-dialog>
  </div>
</template>

<script setup>
import NavBar from '../../components/NavBar'
import Footer from "../../components/Footer";
import Icon from "../../components/icon";
import {ref} from "vue";

const selectBank = ref(false)
</script>