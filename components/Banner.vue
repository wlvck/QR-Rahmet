<template>
  <div class="limit__container">
    <div class="banner__container">
      <div class="content flex-grow-1 flex-shrink-1">
        <h1>Оплата и чаевые
          в один клик</h1>
        <p>Подключите свое заведение к сервису или отправьте чаевые  сотруднику, которого хотите отблагодарить</p>
        <div class="buttons">
          <v-btn elevation="0">Подключить заведение</v-btn>
          <v-btn elevation="0">Оставить чаевые</v-btn>
        </div>
      </div>
      <div>
        <img class="terminalImage" src="../assets/images/banner.png" alt="">
        <div class="rectangle"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Banner"
}
</script>