<template>
  <div class="carousel">
    <div class="limit__container">
      <h1>Для всех</h1>
      <div class="d-flex">
        <v-btn elevation="0" :class="{activeSlide: currentIndex === 0}" class="slider__btn" @click="updateSlide(0)">
          Ресторанам
        </v-btn>
        <v-btn elevation="0" :class="{activeSlide: currentIndex === 1}" class="slider__btn" @click="updateSlide(1)">
          Гостям
        </v-btn>
        <v-btn elevation="0" :class="{activeSlide: currentIndex === 2}" class="slider__btn" @click="updateSlide(2)">
          Сотрудникам
        </v-btn>
      </div>
      <div class="carousel__wrapper">
        <div class="carousel__container" :style="{'margin-left': '-' + (100*currentIndex)+'%'}">
          <div class="carousel__item" v-for="img in 3">
            <img alt="" :src="`/_nuxt/assets/images/slide${img}.png`"/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Carousel",
  data() {
    return {
      currentIndex: 0,
      colors: [
        'primary',
        'secondary',
        'yellow darken-2',
        'red',
        'orange',
      ],
      model: 0,
    }
  },
  methods: {
    updateSlide(whichIndex) {
      this.currentIndex = whichIndex
    }
  }
}
</script>

<style lang="scss">
.carousel {
  margin: 96px 0;

  h1 {
    margin: 0 0 40px 0;
    font-weight: 700;
    font-size: 48px;
    line-height: 56px;
  }

  .v-btn:first-child {
    padding: 0 !important;
    margin-bottom: 40px;
  }
}

.carousel__wrapper {
  max-width: 845px;
  //margin-left: 20%;

  img {
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -o-user-select: none;
    user-select: none;
  }
}

.activeSlide {
  position: relative;
  transition: all ease 0.5s;

  &::before {
    content: '';
    transition: all ease 0.5s;
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    background: #DDAC00;
    height: 4px;
  }
}

.carousel__container {
  display: flex;
  transition: all ease .5s;
}

.carousel__item {
  margin: 0 24px 0 0;
  max-width: 845px;
  width: 100%;
}

.slider__btn {
  font-weight: 400;
  font-size: 20px;
  text-transform: capitalize;
  line-height: 28px;
  text-align: center;
  color: #55534E;
}
</style>