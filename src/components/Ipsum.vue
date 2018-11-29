<template>
  <section>
    <div v-if="!show">
      <button @click="show = true">Add an Ipsum</button>
    </div>
    <div v-else>
      <h2>Add a New Ipsum</h2>
      <IpsumForm v-show="true" v-bind:ipsum="ipsum"/>
        
    </div>
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
  },
  methods: {
    handleAdd(ipsum) {
      this.show = false;
      this.onAdd(ipsum);
    }
  }

};
</script>

<style>

</style>