<template>
  <div class="d-flex flex-column page">
    <NavBar/>
    <div class="flex-shrink-1 main__container flex-grow-1">
      <div class="account__container limit__container">
        <h1>Ресторан Дареджани</h1>
        <div class="container__header">
          <v-tabs v-model="tab" align-tabs="title">
            <v-tab :value="1">Сотрудники</v-tab>
            <v-tab :value="2">Отзывы</v-tab>
          </v-tabs>
          <div class="header__buttons d-flex">
            <v-btn elevation="0" @click.prevent="addEmployee = true">
              <icon class="mr-4" icon-name="plus"/>
              Добавить сотрудника
            </v-btn>
            <v-btn elevation="0">
              <icon class="mr-4" icon-name="plus"/>
              Выгрузить отчет
            </v-btn>
          </div>
        </div>
        <v-window v-model="tab">
          <v-window-item :value="1">
            <div class="search__block">
              <icon class="mr-3" icon-name="search"/>
              <input type="text" placeholder="Поиск сотрудника по имени или ID"/>
            </div>
            <v-table fixed-header
                     height="500">
              <thead>
              <tr>
                <th class="text-left">
                  ID сотрудника
                </th>
                <th class="text-center">
                  ФИО сотрудника
                </th>
                <th class="text-center">
                  Сумма полученных чаевых
                </th>
                <th class="text-center">
                  Рейтинг
                  <icon icon-name="sort-arrow"/>
                </th>
                <th class="text-center">
                  Удаление сотрудника
                </th>
              </tr>
              </thead>
              <tbody>
              <tr
                  v-for="item in 15"
                  :key="item"
              >
                <td>556424</td>
                <td class="text-center">Абзалов Данияр</td>
                <td class="text-center">2 000 ₸</td>
                <td class="text-center">5
                  <icon icon-name="star"/>
                </td>
                <td class="text-center">
                  <icon class="pointer" icon-name="trash" @click="deleteEmployee = true"/>
                </td>
              </tr>
              </tbody>
            </v-table>
          </v-window-item>
          <v-window-item :value="2">
            <div class="search__block">
              <icon class="mr-3" icon-name="search"/>
              <input type="text" placeholder="Поиск сотрудника по имени или ID"/>
            </div>
            <v-table fixed-header
                     height="500">
              <thead>
              <tr>
                <th class="text-left">
                  Дата
                </th>
                <th class="text-center">
                  Отзыв
                </th>
                <th class="text-center">
                  ФИО сотрудника
                </th>
                <th class="text-center">
                  ID сотрудника
                </th>
                <th class="text-center">
                  Рейтинг
                  <icon icon-name="sort-arrow"/>
                </th>
              </tr>
              </thead>
              <tbody>
              <tr
                  v-for="item in 15"
                  :key="item"
              >
                <td>06.02.2023</td>
                <td class="text-center">Все круто, спасибо за такой прием</td>
                <td class="text-center">Абзалов Данияр</td>
                <td class="text-center">556424</td>
                <td class="text-center">5
                  <icon icon-name="star"/>
                </td>
              </tr>
              </tbody>
            </v-table>
          </v-window-item>
        </v-window>
      </div>
    </div>
    <Footer/>
    <v-dialog width="456px" v-model="addEmployee">
      <v-card class="modal__container add__employee">
        <div class="d-flex justify-end pointer" @click.prevent="addEmployee = false">
          <icon icon-name="close"/>
        </div>
        <div class="modal__title">
          Добавить сотрудника
        </div>
        <h5 class="mt-3 mb-6">ID сотрудника: 156-545</h5>
        <v-card-text class="mb-0">
          Отправьте ссылку ниже сотруднику.
          Сотрудник пройдет регистрацию по ссылке
        </v-card-text>
        <v-btn class="mt-4 secondary__btn" elevation="0">
          <icon icon-name="link"/>
          Скопировать ссылку
        </v-btn>
      </v-card>
    </v-dialog>
    <v-dialog width="456px" v-model="deleteEmployee">
      <v-card class="modal__container">
        <h4 class="mt-3 mb-6">Удалить сотрудника
          Абзалов Данияр (ID - 556435)?</h4>
        <div class="delete__group">
          <v-btn class="secondary__btn flex-shrink-1 flex-grow-1" elevation="0" @click="deleteEmployee = false">
            Отмена
          </v-btn>
          <v-btn class="primary__btn flex-shrink-1 flex-grow-1" elevation="0" @click="deleteEmployee = false">
            Да, удалить
          </v-btn>
        </div>
      </v-card>
    </v-dialog>
  </div>
</template>

<script setup>
import NavBar from '../../components/NavBar'
import Footer from "../../components/Footer";
import {ref} from "vue";
import Icon from "../../components/icon";

const tab = ref()
const addEmployee = ref(false)
const deleteEmployee = ref(false)
</script>