<template>
<component :is="iconName"/>
</template>

<script>
import logo from "./icons/logo";
import arrowDown from "./icons/arrowDown";
import menuToggle from "./icons/menuToggle";
export default {
  name: "icon",
  props: [
      'iconName'
  ],
  components: {
    logo,
    arrowDown,
    menuToggle,
  }
}
</script>

<style scoped>

</style>