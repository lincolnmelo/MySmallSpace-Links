<template>
  <div class="row">
    <Card :loja="item.loja" :titulo="item.titulo" :categoria="item.categoria" :linkItem="item.linkItem"
      v-for="item in this.dataCards" :key="item.loja" />
  </div>
</template>

<script>
import Card from "../cards/Card.vue";

export default {
  name: "Cards",
  props:{
    dataCards:{
          type:[Array,Object],
          required:true,
        },
  },
  components: {
    Card,
  }
};
</script>

<style scoped>
.row {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  flex-basis: 100%;
  --bs-gutter-x: 0rem;
}
</style>
