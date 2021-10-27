<template>
  <div class="row">
    <Card
      :title="item.title"
      :label="item.label"
      :imgUrl="item.imgUrl"
      :link="item.link"
      v-for="item in indications"
      :key="item.title"
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
