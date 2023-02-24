<template>
  <div class="limit__container">
    <div class="banner__container">
      <div class="content flex-grow-1 flex-shrink-1">
        <h1>Оплата и чаевые
          в один клик</h1>
        <p>Подключите свое заведение к сервису или отправьте чаевые сотруднику, которого хотите отблагодарить</p>
        <div class="buttons">
          <v-btn elevation="0">Подключить заведение</v-btn>
          <v-btn elevation="0" @click.prevent="dialog = true">Оставить чаевые</v-btn>
        </div>
      </div>
      <div>
        <img class="terminalImage" src="../assets/images/banner.png" alt="">
        <div class="rectangle"></div>
      </div>
    </div>
    <v-dialog
        v-model="dialog"
        width="max-content"
    >
      <v-card class="modal__container">
        <div class="d-flex justify-end">
          <icon class="close pointer" icon-name="close" @click="dialog = false"/>
        </div>
        <v-card-title>
          Добро пожаловать!
        </v-card-title>
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
  </div>
</template>

<script setup>
import VOtpInput from 'vue3-otp-input';
import {ref, watch} from "vue";
import Icon from "./icon";

const filled = ref(false)
const dialog = ref(false)
const handleOnComplete = (value) => {
}
const handleOnChange = (value) => {
  filled.value = value.length === 6
}
</script>