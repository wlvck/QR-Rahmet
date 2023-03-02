<template>
  <div class="navbar__container" :class="route.name === 'index' ? 'py-10' : 'py-6'">
    <div class="limit__container navbar__items d-flex align-center justify-space-between">
      <Icon class="pointer" icon-name="logo" @click="$router.push('/')"/>
      <ul class="navbar__items d-flex align-center">
        <li v-if="route.name === 'index'">Как это работает</li>
        <li v-if="route.name === 'index'">Для кого</li>
        <li v-if="route.name === 'index'">Управление</li>
        <li v-if="route.name === 'index'">Преимущества</li>
        <li v-if="route.name === 'index'">Контакты</li>
        <li class="locale">Рус
          <icon class="ml-2" icon-name="arrow-down"/>
          <div class="languages">
            <p>Каз</p>
            <p>Eng</p>
          </div>
        </li>
        <li class="menu__toggle ml-7" @click="isMenuOpen = !isMenuOpen">
          <icon :icon-name="isMenuOpen ? 'close' : 'menu-toggle'"/>
        </li>
        <li v-if="route.name !== 'index'" class="restaurant__logo">
          <img src="../assets/images/restaurant-logo.png" alt="">
          <h3>Ресторан Дареджани</h3>
        </li>
      </ul>
    </div>
    <transition name="slide-fade">
      <ul v-if="isMenuOpen" class="mobile__menuItems d-flex flex-column">
        <li>Как это работает</li>
        <li>Для кого</li>
        <li>Управление</li>
        <li>Преимущества</li>
        <li>Контакты</li>
      </ul>
    </transition>
  </div>
</template>

<script setup>
import Icon from "./icon";
import {ref} from 'vue'
import {useRoute} from "nuxt/app";

const route = useRoute()
let isMenuOpen = ref(false)
</script>