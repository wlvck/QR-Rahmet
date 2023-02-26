<template>
  <div class="d-flex flex-column page">
    <NavBar/>
    <div class="flex-shrink-1 main__container flex-grow-1">
      <div class="account__container limit__container">
        <h1 class="text-center">Профиль</h1>
        <div class="application__container profile__container">
          <v-row no-gutters>
            <v-col lg="3" sm="3" cols="12">
              <div class="d-flex">
                <div class="mr-4">
                  <img src="../../assets/images/profile.png" alt="">
                  <div class="edit">Изменить</div>
                </div>
                <div class="profile__name-mobile">Абзалов Алдияр Амантаевич</div>
              </div>
            </v-col>
            <v-col lg="9" sm="9" cols="12">
              <h4 class="profile__name-desktop">Абзалов Алдияр Амантаевич</h4>
              <v-divider class="my-4 mobile-divider"/>
              <v-row class="info__row">
                <v-col lg="4" sm="4" cols="12">
                  <div class="info__title">ID</div>
                  <div class="info__data">546324</div>
                </v-col>
                <v-col lg="4" sm="4" cols="12">
                  <div class="info__title">Баланс</div>
                  <div class="info__data">2 000 ₸</div>
                </v-col>
                <v-col lg="4" sm="4" cols="12">
                  <div class="info__title">Рейтинг</div>
                  <div class="info__data">5
                    <icon icon-name="star"/>
                  </div>
                </v-col>
              </v-row>
            </v-col>
          </v-row>
          <v-divider class="my-6"/>
          <v-form>
            <v-row>
              <v-col lg="6" sm="6" cols="12">
                <v-text-field class="mb-4" label="ИИН"/>
                <v-text-field label="Номер телефона"/>
              </v-col>
              <v-col lg="6" sm="6" cols="12">
                <v-text-field label="ФИО"/>
              </v-col>
            </v-row>
            <v-divider class="my-6"/>
            <v-row>
              <v-col lg="6" sm="6" cols="12">
                <v-btn elevation="0" class="primary__btn">Вывести средства</v-btn>
              </v-col>
              <v-col lg="6" sm="6" cols="12">
                <v-btn elevation="0" class="secondary__btn">Изменить пароль</v-btn>
              </v-col>
            </v-row>
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
import {ref} from "vue";
import Icon from "../../components/icon";
</script>