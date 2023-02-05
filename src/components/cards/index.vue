<template>
  <div class="row">
    <Card
      :loja="item.loja"
      :titulo="item.titulo"
      :categoria="item.categoria"
      :linkItem="item.linkItem"
      v-for="item in indications"
      :key="item.loja"
    />
  </div>
</template>

<script>
import Card from "../cards/Card.vue";
import { Indications } from "../../services/getIndications";

export default {
  name: "Cards",
  components: {
    Card,
  },
  setup() {
    const indications = Indications;
    return { indications };
  },
};
</script>

<style scoped>
.row {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  flex-basis: 100%;
}
</style>
