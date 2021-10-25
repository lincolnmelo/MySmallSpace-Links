<template>
    <div class="card pink">
      <h2>{{title}}</h2>
      <p>{{label}}</p>
      <img
        class="image"
        v-bind:src="`${imgUrl}`"
        alt=""
      />
    </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    title: String,
    label: String,
    imgUrl: String
  }
};
</script>

<style scoped>
.CardComponent {
  color: #ffc4ca;
  font-weight: bold;
}

body {
  font-family: "Poppins", sans-serif;
  background-color: #fafafa;
}

.card {
  border-radius: 5px;
  box-shadow: 7px 7px 13px 0px rgba(50, 50, 50, 0.22);
  padding: 15px;
  margin: 15px;
  width: 400px;
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
  max-width: 64px;
  max-height: 64px;
}

.pink {
  border-left: 3px solid #ffc4ca;
}
</style>