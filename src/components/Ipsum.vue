<template>
  <section>
    <IpsumDetail v-bind:ipsum="ipsum"/>
  </section>
</template>

<script>
import IpsumDetail from './IpsumDetail.vue';

export default {
  data() {
    return {
      show: false
    };
  },
  props: {
    ipsum: Object,
    onAdd: Function
  },
  components: {
    IpsumDetail
  }
};
</script>
