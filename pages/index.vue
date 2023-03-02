<template>
  <div class="d-flex flex-column page">
    <NavBar/>
    <div class="flex-shrink-1 flex-grow-1">
      <Banner/>
      <WorkProcess/>
      <Advantages/>
      <Carousel/>
      <FunctionalOffice/>
      <Partners/>
    </div>
    <Footer/>
  </div>
</template>

<script setup>
import NavBar from '/components/NavBar'
import Footer from "../components/Footer";
import Banner from "../components/Banner";
import WorkProcess from "../components/WorkProcess";
import Advantages from "../components/Advantages";
import Carousel from "../components/Carousel";
import FunctionalOffice from "../components/FunctionalOffice";
import Partners from "../components/Partners";
</script>