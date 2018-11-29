<template>
  <section>
    <IpsumDetail
      v-bind:ipsum="ipsum"/>
  </section>
</template>
<script>
/*like animal detail*/
import IpsumDetail from './IpsumDetail.vue';
import IpsumForm from './IpsumForm.vue';
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
    IpsumDetail,
    IpsumForm
  }

};
</script>

<style>

</style>