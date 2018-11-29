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
    onAdd: Function
  }
};
</script>

<style>
  form {
    text-align: center;
    margin-left: 10%;
  }
  button {
    border: 2px solid black;
    border-radius: 5px;
  }
  span {
    width: 190px;
    display: inline-block;
  }
  input, textarea {
    width: 450px;
  }
  label {
    display: flex;
    padding: 10px;
    font-size: 1.2em;
    font-weight: bold;
  }
  textarea {
    height: 100px;
  }
</style>
