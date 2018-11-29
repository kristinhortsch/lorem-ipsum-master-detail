<template>
  <section class="form-section">
    <div v-if="!show">
      <p>Click on the button to create a new ipsum to add to the list!</p>
      <button @click="show = true">Add an Ipsum</button>
    </div>
    <div v-else>
      <h2>Add a New Ipsum</h2>
      <IpsumForm class="form"
        :onAdd="handleAdd"
        :onCancel="() => show = false"/>
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

<style scoped>
  .form-section {
    border: 3px solid gray;
    margin: 5px 0px 15px 0px;
    text-align: center;
  }

  button {
    border: 2px solid black;
    border-radius: 5px;
    margin: 5px;
    font-size: 0.8em;
  }

  h2 {
    padding-bottom: 5px;
    margin: 0px;
    font-weight: 550;
    color: navy;
  }

  .form {
    margin: 0px auto;
    padding: 0px;
  }
</style>
