<template>
  <div class="loginForm">
    <h1>{{ msg }}</h1>
    
  </div>
</template>

<script>
export default {
  name: 'LoginForm',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: blue;
}
</style>
