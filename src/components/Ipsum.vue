<template>
  <section>
    <IpsumDetail
      v-if="!edit"
      v-bind:ipsum="ipsum"/>
  </section>
</template>
<script>
/*like animal detail*/
import IpsumDetail from './IpsumDetail.vue';
// import IpsumForm from './IpsumForm.vue';
export default {
  data() {
    return {
      edit: false
    };
  },
  props: {
    ipsum: Object
  },
  components: {
    IpsumDetail
    // IpsumForm
  }

};
</script>

<style>

</style>