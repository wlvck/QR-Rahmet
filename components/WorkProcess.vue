<template>
  <div class="limit__container" id="howDoesItWork">
    <div class="d-flex align-center justify-space-between work__process">
      <img src="../assets/images/iphone.png" alt="">
      <div class="process__content">
        <h3>Как это работает?</h3>
        <ul>
          <li class="d-flex">
            <icon icon-name="checked-mark" class="mr-4"/>
            <div>
              <h4>Разместите QR в заведениях</h4>
              <p>На разных видах носителя</p>
            </div>
          </li>
          <li class="d-flex">
            <icon icon-name="un-checked-mark" class="mr-4"/>
            <div>
              <h4>Гости оставляют отзыв и чаевые на сайте</h4>
              <p>Без приложения и регистрации</p>
            </div>
          </li>
          <li class="d-flex">
            <icon icon-name="un-checked-mark" class="mr-4"/>
            <div>
              <h4>Моментальный вывод безналичных и чаевых</h4>
              <p>Для работников заведения</p>
            </div>
          </li>
          <li class="d-flex">
            <icon icon-name="un-checked-mark" class="mr-4"/>
            <div>
              <h4>Детальная статистика для ресторана</h4>
              <p>Данные об отзывах и чаевых </p>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
import Icon from "./icon";

export default {
  components: {Icon}
}
</script>