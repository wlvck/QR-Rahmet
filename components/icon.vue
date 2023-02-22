<template>
<component :is="iconName"/>
</template>

<script>
import logo from "./icons/logo";
import arrowDown from "./icons/arrowDown";
import menuToggle from "./icons/menuToggle";
import instagram from "./icons/instagram";
import whatsapp from "./icons/whatsapp";
import telegram from "./icons/telegram";
import mail from "./icons/mail";
import phone from "./icons/phone";
export default {
  name: "icon",
  props: [
      'iconName'
  ],
  components: {
    logo,
    arrowDown,
    menuToggle,
    instagram,
    phone,
    telegram,
    whatsapp,
    mail,
  }
}
</script>

<style scoped>

</style>