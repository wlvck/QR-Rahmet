<template>
  <div class="advantages__container limit__container">
    <h1>Преимущества</h1>
    <div class="items__block">
      <div class="block__item">
        <icon icon-name="bar-graph"/>
        <h4>Настройка платформы под ключ</h4>
        <p>Micros, iiko, r-keeper, TillyPad, quickresto и т.п.Обучение займет не более 30 мин</p>
      </div>
      <div class="block__item">
        <icon icon-name="device"/>
        <h4>Доступно для телефонов
          и компьютеров</h4>
        <p>Можно пользоваться сервисом через любые мобильные и компьютерные устройства</p>
      </div>
      <div class="block__item">
        <icon icon-name="circle-heart"/>
        <h4>Абсолютно бесплатно
          для заведения</h4>
        <p>Легкая и быстрая настройка работы платформы без абонентской платы</p>
      </div>
      <div class="block__item">
        <icon icon-name="head-phone"/>
        <h4>Тех. поддержка</h4>
        <p>Тех. поддержка работает для качеством контроля сервиса и ответов на вопросы</p>
      </div>
      <div class="block__item">
        <icon icon-name="user"/>
        <h4>Личный кабинет
          для руководителя</h4>
        <p>Контроль сотрудников, работа с лояльностью гостей и аналитика по чаевым в одном месте</p>
      </div>
      <div class="block__item">
        <icon icon-name="add-user"/>
        <h4>Персональный менеджер
          для заведения</h4>
        <p>Вы сможете обращаться к нему за помощью по управлению системой</p>
      </div>

    </div>
  </div>
</template>

<script>
import Icon from "./icon";
export default {
  name: "Advantages",
  components: {Icon}
}
</script>

<style scoped>

</style>