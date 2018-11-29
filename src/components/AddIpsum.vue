<template>
  <section class="form-section">
    <div v-if="!show">
      <p>Click on the button to create a new ipsum to add to the list!</p>
      <button @click="show = true">Add an Ipsum</button>
    </div>
    <div v-else>
      <h2>Add a New Ipsum</h2>
      <IpsumForm
        :onAdd="handleAdd"/>
    </div>
  </section>
</template>

<script>
import IpsumForm from './IpsumForm';
export default {
  data() {
    return {
      show: false
    };
  },
  components: {
    IpsumForm
  },
  props: {
    onAdd: Function
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
  .form-section {
    border: 3px solid gray;
    margin: 5px 0px 15px 0px;
    padding: 20px;
    text-align: center;

  }

  

</style>
