<template>
  <button class="button">
    <span>{{ text || "My Buttom" }} </span>
  </button>
</template>

<script>
export default {
  name: "CustomButton",
  props: {
    text: String,
  },
};
</script>

<style>
.button {
  border-radius: 10px;
  background-color: #ffc4ca;
  border: none;
  color: #ffffff;
  font-weight: bold;
  text-align: center;
  font-size: 16px;
  padding: 15px;
  transition: all 0.5s;
  cursor: pointer;
  margin: 5px;
}
</style>