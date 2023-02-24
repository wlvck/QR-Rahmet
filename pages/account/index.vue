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
          <div class="header__buttons">
            <v-btn elevation="0"><icon class="mr-4" icon-name="plus"/>Добавить сотрудника</v-btn>
            <v-btn elevation="0"><icon class="mr-4" icon-name="plus"/>Выгрузить отчет</v-btn>
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
                  Рейтинг <icon icon-name="sort-arrow"/>
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
                <td class="text-center">5 <icon icon-name="star"/></td>
                <td class="text-center"><icon icon-name="trash"/></td>
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
                  ID сотрудника
                </th>
                <th class="text-center">
                  ФИО сотрудника
                </th>
                <th class="text-center">
                  Сумма полученных чаевых
                </th>
                <th class="text-center">
                  Рейтинг <icon icon-name="sort-arrow"/>
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
                <td class="text-center">5 <icon icon-name="star"/></td>
                <td class="text-center"><icon icon-name="trash"/></td>
              </tr>
              </tbody>
            </v-table>
          </v-window-item>
        </v-window>
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

const tab = ref(1)
</script>