<template>
  <div class="footer__container">
    <div class="limit__container">
      <v-row no-gutters>
        <v-col
            class="footer__col"
            cols="12"
            md="4"
        >
          <div class="col__header">
            Сотрудничество
          </div>
          <div class="contact__block d-flex">
            <icon icon-name="phone" class="mr-4"/>
            <div>
              <a href="tel:87071431070">+ 7 (798) 849 43 45</a>
              <p>Пн - Вс 10.00 - 19.00</p>
            </div>
          </div>
          <div class="contact__block d-flex">
            <icon icon-name="mail" class="mr-4"/>
            <div>
              <a href="mail:qrrahment@gmail.com">qrrahment@gmail.com</a>
            </div>
          </div>
          <div class="contact__block d-flex">
            <icon icon-name="whatsapp" class="mr-4"/>
            <div>
              <a href="tel:87071431070">8 (708) 434 59 05</a>
            </div>
          </div>
          <div class="contact__block d-flex">
            <icon icon-name="telegram" class="mr-4"/>
            <div>
              <a href="#">qrrahment</a>
            </div>
          </div>
          <div class="contact__block d-flex">
            <icon icon-name="instagram" class="mr-4"/>
            <div>
              <a href="#">qrrahment</a>
            </div>
          </div>
        </v-col>
        <v-col
            class="footer__col"
            cols="12"
            md="4"
        >
          <div class="col__header">
            Техническая поддержка
          </div>
          <div class="contact__block d-flex">
            <icon icon-name="phone" class="mr-4"/>
            <div>
              <a href="tel:87071431070">+ 7 (798) 849 43 45</a>
              <p>Пн - Вс 10.00 - 19.00</p>
            </div>
          </div>
          <div class="contact__block d-flex">
            <icon icon-name="mail" class="mr-4"/>
            <div>
              <a href="mail:qrahment@gmail.com">qrrahment@gmail.com</a>
            </div>
          </div>
          <div class="contact__block d-flex">
            <icon icon-name="whatsapp" class="mr-4"/>
            <div>
              <a href="tel:87071431070">8 (708) 434 59 05</a>
            </div>
          </div>
          <div class="contact__block d-flex">
            <icon icon-name="telegram" class="mr-4"/>
            <div>
              <a href="#">qrrahment</a>
            </div>
          </div>
          <div class="contact__block d-flex">
            <icon icon-name="instagram" class="mr-4"/>
            <div>
              <a href="#">qrrahment</a>
            </div>
          </div>
        </v-col>
        <v-col
            class="footer__col"
            cols="12"
            md="4"
        >
          <div class="col__header">
            Полезные ссылки
          </div>
          <div class="useful__links">
            <a href="#">Вход для сотрудников заведений</a>
            <a href="#">Вход для управляющих заведений</a>
            <a href="#">Политика конфиденциальности</a>
            <a href="#">Условия пользования</a>
            <a href="#">Установка и возможности сервиса</a>
          </div>
        </v-col>
      </v-row>
      <p class="rightsReserved">©2023 QRRahmet. Все права защищены.</p>
    </div>
  </div>
</template>
<script>
import Icon from "./icon";
export default {
  components: {Icon}
}
</script>