<template>
  <div class="limit__container">
    <div class="banner__container">
      <div class="content flex-grow-1 flex-shrink-1">
        <h1>Оплата и чаевые
          в один клик</h1>
        <p>Подключите свое заведение к сервису или отправьте чаевые сотруднику, которого хотите отблагодарить</p>
        <div class="buttons">
          <v-btn elevation="0" @click.prevent="addRestaurant = true">Подключить заведение</v-btn>
          <v-btn elevation="0" @click.prevent="leaveTip = true">Оставить чаевые</v-btn>
        </div>
      </div>
      <div>
        <img class="terminalImage" src="../assets/images/banner.png" alt="">
        <div class="rectangle"></div>
      </div>
    </div>
    <v-dialog
        v-model="leaveTip"
        width="max-content"
    >
      <v-card class="modal__container tipLimit">
        <div class="d-flex justify-end">
          <icon class="close pointer" icon-name="close" @click="leaveTip = false"/>
        </div>
        <div class="modal__title">
          Добро пожаловать!
        </div>
        <v-card-text class="mt-1">
          Пожалуйста, введите код официанта, чтобы оставить чаевые или отзыв
        </v-card-text>
        <div class="d-flex flex-row justify-center otp">
          <v-otp-input
              ref="otpInput"
              input-classes="otp-input"
              separator="-"
              :num-inputs="6"
              :should-auto-focus="true"
              :is-input-num="true"
              :conditionalClass="['one', 'two', 'three', 'four', 'five', 'six']"
              :placeholder="['X', 'X', 'X', 'X', 'X', 'X']"
              @on-change="handleOnChange"
              @on-complete="handleOnComplete"
          />
        </div>
        <v-btn
            :disabled="!filled"
            elevation="0">
          Продолжить
        </v-btn>
      </v-card>
    </v-dialog>
    <v-dialog
        v-model="addRestaurant"
        width="max-content"
    >
      <v-card class="modal__container restaurantLimit">
        <div class="d-flex justify-end">
          <icon class="close pointer" icon-name="close" @click="addRestaurant = false"/>
        </div>
        <div class="modal__title">
          Хочу подключить заведение к QR Rahmet
        </div>
        <div class="restaurant__info">
          <div class="info__block">
            <icon icon-name="discount"/>
            <h4>До 30% доп. чаевых</h4>
            <p>Их точно станет больше, мы проверяли!</p>
          </div>
          <div class="info__block">
            <icon icon-name="circle-heart"/>
            <h4>До 30% доп. чаевых</h4>
            <p>Их точно станет больше, мы проверяли!</p>
          </div>
        </div>
        <v-divider></v-divider>
        <v-card-text>
          Заполните форму и мы с вами свяжемся с вами с 10.00 до 19.00 по Астане
        </v-card-text>
        <v-form class="form__grid">
          <v-text-field
              label="Название вашего заведения"
          >

          </v-text-field>
          <v-text-field
              label="Адрес заведения"
          >

          </v-text-field>
          <v-text-field
              label="Ваше имя"
          >

          </v-text-field>
          <v-text-field
              label="Номер телефона"
          >

          </v-text-field>
        </v-form>
        <div class="modal__buttons d-flex align-center">
          <v-btn
              elevation="0">
            Оставить заявку
          </v-btn>
          <v-btn
              elevation="0">
            Связаться по WhatsApp
          </v-btn>
        </div>
      </v-card>
    </v-dialog>
  </div>
</template>

<script setup>
import VOtpInput from 'vue3-otp-input';
import {ref, watch} from "vue";
import Icon from "./icon";

const filled = ref(false)
const leaveTip = ref(false)
let addRestaurant = ref(false)
const handleOnComplete = (value) => {
}
const handleOnChange = (value) => {
  filled.value = value.length === 6
}
</script>