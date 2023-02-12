<template>
  <navBar text="My Small Space" />
  <customFooter />
</template>

<script>
import navBar from './navbar/navBar.vue';
import customFooter from './shared/customFooter.vue';

export default {
  name: "MainPage",
  components: {
    navBar,
    customFooter
  },
  props: {
    msg: String,
  },
};
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #ffc4ca;
  text-decoration: none;
}
</style>
