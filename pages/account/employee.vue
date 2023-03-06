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
            <div class="employee__grid">
              <v-text-field label="ИИН"/>
              <v-text-field label="ФИО"/>
              <v-text-field label="Номер телефона"/>
            </div>
            <v-divider class="my-6"/>
            <v-row>
              <v-col lg="6" sm="6" cols="12">
                <v-btn elevation="0" class="primary__btn" @click="withdraw = true">Перевести</v-btn>
              </v-col>
              <v-col lg="6" sm="6" cols="12">
                <v-btn elevation="0" class="secondary__btn" @click="password = true">Изменить пароль</v-btn>
              </v-col>
            </v-row>
          </v-form>
        </div>
      </div>
    </div>
    <Footer/>
    <v-dialog v-model="withdraw" width="468px">
      <div class="modal__container">
        <div class="d-flex justify-end">
          <icon class="pointer" icon-name="close" @click="withdraw = false"/>
        </div>
        <div class="modal__title mb-6">
          Вывести средства
        </div>
        <v-form>
          <v-text-field label="Номер карты"/>
          <v-row class="mt-4">
            <v-col cols="6">
              <v-text-field label="Срок действия"/>
            </v-col>
            <v-col cols="6">
              <v-text-field label="CVV/CVC"/>
            </v-col>
          </v-row>
          <v-btn elevation="0" class="primary__btn mt-6">
            Вывести
          </v-btn>
        </v-form>
      </div>
    </v-dialog>
    <v-dialog v-model="password" width="468px">
      <div class="modal__container">
        <div class="d-flex justify-end">
          <icon class="pointer" icon-name="close" @click="password = false"/>
        </div>
        <div class="modal__title mb-6">
          Изменить пароль
        </div>
        <v-form>
          <v-text-field label="Старый пароль"/>
          <v-text-field class="my-4" label="Новый пароль"/>
          <v-text-field label="Повторите новый пароль"/>
          <v-btn elevation="0" class="primary__btn mt-6">
            Сохранить
          </v-btn>
        </v-form>
      </div>
    </v-dialog>
  </div>
</template>

<script setup>
import NavBar from '../../components/NavBar'
import Footer from "../../components/Footer";
import {ref} from "vue";
import Icon from "../../components/icon";
const withdraw = ref(false)
const password = ref(false)
</script>