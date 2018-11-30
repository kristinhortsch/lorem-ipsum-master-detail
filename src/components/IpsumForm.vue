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

      <label class="button">
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
    justify-content: center;
  }
  button {
    border: 2px solid black;
    border-radius: 5px;
    margin: 5px;
    font-size: 0.75em;
  }

  .button {
    display: block;
  }

  span {
    display: inline-block;
  }

  input, textarea {
    height: 20px;
    width: 13vw;
  }

  label {
    display: flex;
    padding: 5px;
    font-size: 1.1em;
    font-weight: 500;
  }

  @media only screen and (max-width: 1160px) {
    form {
      text-align: center;
      display: flex;
      justify-content: center;
      flex-direction: column;
      margin-left: 5%;
    }

    span {
      width: 90px;
    }
    input, textarea {
    width: 60vw;
    height: 20px;
  }

  }
</style>
