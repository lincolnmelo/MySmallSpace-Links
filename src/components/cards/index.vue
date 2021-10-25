<template>
  <Card/>
</template>

<script>
import Card from '../cards/Card.vue';

export default {
  name: 'Cards',
  props: {
    msg: String
  },
  components: {
    Card
  }
}
</script>
