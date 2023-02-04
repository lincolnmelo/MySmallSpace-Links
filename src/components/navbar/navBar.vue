<template>
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
              Lojas
            </a>
            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
              <li><a class="dropdown-item" href="#">Amazon</a></li>
            </ul>
          </li>
        </ul>
        <form class="d-flex">
          <input class="form-control me-2" type="search" placeholder="" aria-label="Search" >
          <button class="btn btn-outline-secondary" type="submit">Pesquisar</button>
        </form>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  props: {
    text: String,
  },
};
</script>

<style>
.navbarmss {
  margin-top: -28px;
  margin-bottom: 25px;
  margin-left: 20px;
  margin-right: 20px;
  border-radius: 10px;
  background-color: #ffffff;
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
</style>