<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <login-form msg="로그인 폼!!" />
    <first-boot />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import LoginForm from './components/LoginForm.vue'
import FirstBoot from './components/FirstBoot.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    LoginForm,
    FirstBoot
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
