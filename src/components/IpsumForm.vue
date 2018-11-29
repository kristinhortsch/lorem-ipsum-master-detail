<template>
  <section>

    <form @submit.prevent="onAdd(ipsum)">
      <label>
        <span>Name:</span>
        <input v-model="ipsum.title" required>
      </label>

      <label>
        <span>Author:</span>
        <input v-model="ipsum.author" required>
      </label>

      <label>
        <span>Category:</span>
        <input v-model="ipsum.category" required>
      </label>

      <label>
        <span>Body:</span>
        <textarea v-model="ipsum.body" required></textarea>
      </label>

      <label>
        <span></span>
        <button type="submit">Add</button>
        <button @click="onCancel" type="button">Cancel</button>
      </label>
    
    </form>
  </section>
</template>

<script>
export default {
  data() {
    return {
      ipsum: {
        title: '',
        author: ''
      }
    };
  },
  props: {
    onAdd: Function,
    onCancel: Function
  }
};
</script>

<style>
  form {
    text-align: center;
    display: flex;
    justify-content: space-evenly;
  }
  button {
    border: 2px solid black;
    border-radius: 5px;
    margin: 5px;
    font-size: 0.75em;
  }

  span {
    display: inline-block;
  }

  input, textarea {
    width: 150px;
    height: 20px;
  }

  label {
    display: flex;
    padding: 5px;
    font-size: 1.1em;
    font-weight: 500;
  }
</style>
