<template>
  <v-row no-gutters v-scroll="onScroll" class="navbar__container d-block" :class="route.name === 'index' ? 'py-10' : 'py-6'">
    <div class="limit__container navbar__items d-flex align-center justify-space-between">
      <Icon class="pointer" icon-name="logo" @click="$router.push('/')"/>
      <ul class="navbar__items d-flex align-center">
        <li v-if="route.name === 'index'"><a class="text-decoration-none" href="#howDoesItWork">Как это работает</a>
        </li>
        <li v-if="route.name === 'index'"><a class="text-decoration-none" href="#forWhom">Для кого</a></li>
        <li v-if="route.name === 'index'"><a class="text-decoration-none" href="#management">Управление</a></li>
        <li v-if="route.name === 'index'"><a class="text-decoration-none" href="#advantages">Преимущества</a></li>
        <li v-if="route.name === 'index'"><a class="text-decoration-none" href="#contacts">Контакты</a></li>
        <li class="locale pointer" style="list-style: none; color: white; padding-left: 16px;">Рус
          <icon class="ml-2" icon-name="arrow-down"/>
          <div class="languages">
            <p>Каз</p>
            <p>Eng</p>
          </div>
        </li>
        <li v-if="route.name === 'index'" class="menu__toggle ml-7" @click="isMenuOpen = !isMenuOpen">
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
        <li @click="isMenuOpen = false"><a class="text-decoration-none text-white" href="#howDoesItWork">Как это
          работает</a>
        </li>
        <li @click="isMenuOpen = false"><a class="text-decoration-none text-white" href="#forWhom">Для кого</a></li>
        <li @click="isMenuOpen = false"><a class="text-decoration-none text-white" href="#management">Управление</a>
        </li>
        <li @click="isMenuOpen = false"><a class="text-decoration-none text-white" href="#advantages">Преимущества</a>
        </li>
        <li @click="isMenuOpen = false"><a class="text-decoration-none text-white" href="#contacts">Контакты</a></li>
      </ul>
    </transition>
  </v-row>
</template>

<script setup>
import Icon from "./icon";
import {ref} from 'vue'
import {useRoute} from "nuxt/app";

const route = useRoute()
let isMenuOpen = ref(false)
let offSetTop = ref(0)
const onScroll = (e) => {
  offSetTop.value = window.scrollY
}

</script>

<style>
</style>