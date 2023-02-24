<template>
  <div class="d-flex flex-column page">
    <NavBar/>
    <div class="flex-shrink-1 flex-grow-1">
      <Banner/>
      <WorkProcess/>
    </div>
    <Footer/>
  </div>
</template>

<script setup>
import NavBar from '/components/NavBar'
import Footer from "../components/Footer";
import Banner from "../components/Banner";
import WorkProcess from "../components/WorkProcess";
</script>