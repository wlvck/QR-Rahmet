<template>
  <div class="limit__container" id="management">
    <div class="functional__container">
      <h1>
        Функциональный кабинет для руководителя
      </h1>
      <div class="items">
        <div class="item">
          <icon icon-name="users"/>
          <h4>Список сотрудников</h4>
        </div>
        <div class="item">
          <icon icon-name="discount"/>
          <h4>Настройка системы
            чаевых</h4>
        </div>
        <div class="item">
          <icon icon-name="book"/>
          <h4>Просмотр рейтинга
            и отзывов</h4>
        </div>
        <div class="item">
          <icon icon-name="bar-graph"/>
          <h4>Подробная аналитика по чаевым и рейтингу</h4>
        </div>
      </div>
      <div class="header__buttons d-flex">
        <v-btn elevation="0">
          Подключить заведение
        </v-btn>
        <v-btn elevation="0">
          Скачать презентацию
        </v-btn>
      </div>
    </div>
  </div>
</template>

<script>
import Icon from "./icon";

export default {
  name: "FunctionalOffice",
  components: {Icon}
}
</script>
