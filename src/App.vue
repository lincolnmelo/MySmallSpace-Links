<template>
    <div id="topPage" class="toppage">
      <img alt="myLogo" class="myLogo" src="./assets/logo-mss.png" />
      <Home msg="My Small Space" />
    </div>
    <navBar text="My Small Space" />
    <Cards />
    <CustomFooter />
</template>

<script>
import Home from "./components/Home.vue";
import Cards from "./components/cards";
import CustomFooter from "./components/shared/customFooter.vue";
import navBar from "./components/navbar/navBar.vue";

export default {
  name: "App",
  components: {
    Home,
    navBar,
    Cards,
    CustomFooter,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
.myLogo {
  box-shadow: 0px 0px 20px #ffbcc3;
  border-radius: 176px;
  background-color: #ffc4ca;
  max-width: 150px;
  margin-top: 30px;
}
.toppage {
  background-color: #ffeef0;
  padding-bottom: 50px;
}

</style>
