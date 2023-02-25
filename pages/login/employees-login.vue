<template>
  <div class="d-flex flex-column page">
    <NavBar/>
    <div class="flex-shrink-1 main__container flex-grow-1">
      <div class="px-4">
        <div class="login__container employee-login__container">
          <h1>Регистрация</h1>
          <v-card-text class="mb-6 mt-3 px-0 py-0">Ваш ID: 546324</v-card-text>
          <v-form class="d-flex">
            <div class="flex-grow-1 flex-shrink-1">
              <v-text-field label="ИИН"/>
              <v-text-field label="ФИО"/>
              <v-divider class="my-6"/>
              <v-text-field label="Номер телефона"/>
              <v-text-field type="password" label="Установите пароль"/>
              <v-text-field type="password" label="Повторите пароль"/>
              <v-btn elevation="0">Зарегистрироваться</v-btn>
            </div>
            <div class="avatar__container">
              <div class="avatar__block d-flex justify-center flex-column align-center">
                <icon icon-name="avatar"/>
                <h4>Добавить фото</h4>
              </div>
              <v-divider/>
            </div>
          </v-form>
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