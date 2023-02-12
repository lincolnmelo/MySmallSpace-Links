<template>
  <div class="contentLogo">
    <img alt="myLogo" class="myLogo" src="../../assets/logo-mss.png" />
    <div class="referenceLogo">
      <p>
        <img src="../../assets/icons/instagram.svg" alt=""
          onclick="window.open('https://www.instagram.com/mysmallspace906', '_blank');">
        <span onclick="window.open('https://www.instagram.com/mysmallspace906', '_blank');"> Beatriz</span>
      </p>
    </div>
  </div>
  <nav class="navbarmss navbar navbar-expand-lg navbar-light">
    <div class="container-fluid">
      <a class="navbar-brand" href="https://www.instagram.com/mysmallspace906" target="_blank">
        <img class="logoname" src="../../assets/imagens/logo_name.png" alt="">
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown"
              aria-expanded="false">
              Itens
            </a>
            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
              <li><a class="dropdown-item" href="#" v-on:click="getItens('todos')">Todos</a></li>
              <li><a class="dropdown-item" href="#" v-on:click="getItens('amazon')">Amazon</a></li>
            </ul>
          </li>
        </ul>
        <form class="d-flex">
          <input class="form-control me-2" type="text" v-model="inputChange" v-on:keydown.enter.prevent='handleSearsh'
            placeholder="" aria-label="Search">
          <button class="btn btn-outline-secondary" type='button' v-on:click="handleSearsh">Pesquisar</button>
        </form>
      </div>
    </div>
  </nav>
  <div :key="cardsKey">
    <Cards :dataCards="this.indications" />
  </div>
</template>

<script>
import Cards from "../../components/cards";
import { Indications } from "@/services/getIndications";
import { ref } from 'vue';

export default {
  name: "Navbar",
  components: {
    Cards
  },
  props: {
    text: String,
  },
  indications: [],
  defealtIndications: [],
  inputChange: String,
  resultSearch: Boolean,
  showModal: Boolean,
  data() {
    return {
      propsCards: this.indications,
    }
  },
  created() {
    this.indications = [...Indications];
    this.defealtIndications = [...Indications];
    this.resultSearch = false;
    this.inputChange = '';
    this.showModal = true;
  },
  setup() {
    const cardsKey = ref(0)

    const renderComponent = () => {
      cardsKey.value++
    }

    return {
      cardsKey,
      renderComponent
    }

  },
  methods: {
    handleSearsh() {
      if (this.inputChange !== undefined) {
        const list = this.defealtIndications.filter((elem) => elem.titulo.toLowerCase().includes(this.inputChange.toLowerCase()));
        list.length ? this.indications = list : this.indications = this.defealtIndications;
      }
      this.renderComponent();
    },
    getItens() {
      this.indications = this.defealtIndications;
      this.renderComponent();
    }
  }
}
</script>

<style>
.navbarmss {
  margin-top: -45px;
  margin-right: 20px;
  margin-bottom: 25px;
  margin-left: 20px;
  border-radius: 10px;
  background-color: white;
}

.logoname {
  margin-top: -4px;
  height: 20px;
}

.form-control {
  border-color: #ffc4ca !important;
}

.form-control:focus {
  box-shadow: inset 0 0 2px #ffc4ca, 0 0 10px #ffc4ca !important;
  color: black !important;
}

.dropdown-menu {
  margin-top: 0 !important;
}

.dropdown-item:focus {
  color: black !important;
  background-color: #fff0f1 !important;
}

.btn-outline-secondary {
  font-weight: bold !important;
}

.btn-outline-secondary:hover {
  border-color: #ffc4ca !important;
  color: black !important;
  background-color: #ffc4ca !important;
}

.contentLogo {
  width: 100%;
  text-align: center;
  margin-bottom: 20px;
  background-color: #fff0f1;
}

.contentLogo a {
  text-decoration: none;
  color: inherit;
}

.myLogo {
  box-shadow: 0px 0px 20px #ffbcc3;
  border-radius: 176px;
  background-color: #ffc4ca;
  max-width: 150px;
  margin-top: 10px;
}

.referenceLogo {
  color: #ffc4ca;
  font-weight: bold;
  margin-top: 10px;
  padding-bottom: 20px;
}

.referenceLogo p img {
  margin-top: -3.5px;
}
</style>