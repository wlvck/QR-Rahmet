<template>
  <div class="d-flex flex-column page">
    <NavBar/>
    <div class="flex-shrink-1 main__container flex-grow-1">
      <div class="px-4">
        <div class="login__container">
          <h1>Вход</h1>
          <div class="error__message" v-if="error">
            Логин или пароль введены неверно.
            Пожалуйста, попробуйте еще раз
          </div>
          <v-form>
            <v-text-field label="Логин"/>
            <v-text-field type="password" label="Пароль"/>
            <v-btn elevation="0" @click="redirect">Войти</v-btn>
          </v-form>
        </div>
      </div>
    </div>
    <Footer/>
  </div>
</template>

<script setup>
import NavBar from '../../components/NavBar'
import Footer from "../../components/Footer";
import {useRouter} from "nuxt/app";
import {ref} from "vue";
const router = useRouter()
const error = ref(false)
const redirect = ()=>{
  router.push('/login/managers-login')
}
</script>