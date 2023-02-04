<template>
  <div class="homeComponent">
    <p>Por: 
      <a
        href="https://www.instagram.com/mysmallspace906"
        target="_blank"
        rel="noopener"
        >Beatriz</a
      >
    </p>
  </div>
</template>

<script>
export default {
  name: "Home",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
.homeComponent {
  color: #ffc4ca;
  font-weight: bold;
  margin-top: 20px;
}
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
