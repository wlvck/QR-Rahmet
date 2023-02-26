<template>
  <div class="navbar__container">
    <div class="limit__container navbar__items d-flex align-center justify-space-between">
      <Icon class="pointer" icon-name="logo" @click="$router.push('/')"/>
      <ul class="navbar__items d-flex align-center">
        <li>Как это работает</li>
        <li>Для кого</li>
        <li>Управление</li>
        <li>Преимущества</li>
        <li>Контакты</li>
        <li class="locale">Рус
          <icon class="ml-2" icon-name="arrow-down"/>
        </li>
        <li class="menu__toggle ml-7" @click="isMenuOpen = !isMenuOpen">
          <icon :icon-name="isMenuOpen ? 'close' : 'menu-toggle'"/>
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

const isMenuOpen = ref(false)
</script>