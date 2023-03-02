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
import search from "./icons/search";
import trash from "./icons/trash";
import plus from "./icons/plus";
import star from "./icons/star";
import link from "./icons/link";
import avatar from "./icons/avatar";
import evStar from "./icons/evStar";
import otherBanks from "./icons/otherBanks";
import kaspi from "./icons/kaspi";
import jusan from "./icons/jusan";
import halyk from "./icons/halyk";
import bcc from "./icons/bcc";
import arrowRight from "./icons/arrowRight";
import forte from "./icons/forte";
import successPayment from "./icons/successPayment";
import sortArrow from "./icons/sortArrow";
import forRestaurant from "./icons/forRestaurant";
import forGuest from "./icons/forGuest";
import forEmployee from "./icons/forEmployee";
export default {
  name: "icon",
  props: [
      'iconName'
  ],
  components: {
    logo,
    forEmployee,
    kaspi,
    successPayment,
    otherBanks,
    arrowDown,
    forGuest,
    forRestaurant,
    arrowRight,
    forte,
    star,
    jusan,
    evStar,
    bcc,
    halyk,
    avatar,
    sortArrow,
    plus,
    menuToggle,
    trash,
    link,
    search,
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