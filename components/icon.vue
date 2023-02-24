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
import checkedMark from "./icons/checkedMark";
import unCheckedMark from "./icons/unCheckedMark";
import addUser from "./icons/addUser";
import circleHeart from "./icons/circleHeart";
import user from "./icons/user";
import headPhone from "./icons/headPhone";
import device from "./icons/headPhone";
import barGraph from "./icons/barGraph";
import users from "./icons/users";
import discount from "./icons/discount";
import book from "./icons/book";
import close from "./icons/close";
export default {
  name: "icon",
  props: [
      'iconName'
  ],
  components: {
    logo,
    arrowDown,
    menuToggle,
    book,
    discount,
    users,
    close,
    barGraph,
    headPhone,
    circleHeart,
    device,
    instagram,
    user,
    phone,
    checkedMark,
    unCheckedMark,
    addUser,
    telegram,
    whatsapp,
    mail,
  }
}
</script>

<style scoped>

</style>