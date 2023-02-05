<template>
  <div class="card pink" v-on:click="redirectLink">
    <span></span>
    <iframe sandbox="allow-popups allow-scripts allow-modals allow-forms allow-same-origin" style="width:120px;height:240px;" marginwidth="0" marginheight="0" scrolling="no" frameborder="0" v-bind:src="`${linkItem}`"></iframe>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    loja: String,
    titulo: String,
    categoria: String,
    linkItem: String,
  },
  methods: {
    redirectLink() {
      window.open(this.link, "_blank");
    },
  },
};
</script>

<style scoped>
body {
  font-family: "Poppins", sans-serif;
  position: relative;
}

.card {
  border-radius: 5px;
  box-shadow: 7px 7px 13px 0px rgba(50, 50, 50, 0.22);
  padding: 15px;
  margin: 15px;
  width: 160px;
  min-height: 170px;
  transition: all 0.3s ease-out;
}

.card:hover {
  transform: translateY(-5px);
  cursor: pointer;
}

.card p {
  color: #a3a5ae;
  font-size: 16px;
}

.image {
  float: right;
  max-width: 35px;
  max-height: 34px;
  position:absolute;
  bottom:0;
}
.pink {
  border-left: 5px solid #ffc4ca;
}

.card span {
  cursor: pointer;
  position: absolute;
  transition: 0.5s;
}

.card span:after {
  content: url("../../assets/icons/login_pink.svg");
  position: fixed;
  padding-top: 15px;
  padding-right: 35px;
  opacity: 0;
  top: 0;
  right: -30px;
  transition: 0.7s;
  color: white;
}

.card:hover span {
  padding-right: 0px;
}

.card:hover span:after {
  opacity: 1;
  right: 0;
}
</style>