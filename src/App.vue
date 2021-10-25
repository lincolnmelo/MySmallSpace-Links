<template>
  <img alt="myLogo" class="myLogo" src="./assets/logo-mss.png">
  <Home msg="My Small Space"/>
  <Cards msg="My Small Space"/>
</template>

<script>
import Home from './components/Home.vue'
import Cards from './components/cards'

export default {
  name: 'App',
  components: {
    Home,
    Cards
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
.myLogo {
  box-shadow:         0px 0px 20px #ffc4ca;
  border-radius: 176px;
  background-color: #ffc4ca;
  max-width: 180px;
}
</style>
