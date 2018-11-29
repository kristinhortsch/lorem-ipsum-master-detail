<template>
  <section>
    <form @submit.prevent="onAdd(ipsum)">
      <label>
        <span>Name:</span>
        <input v-model="ipsum.title" required>
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
        title: ''
      }
    };

  },
  props: {
    onAdd: Function
  }
};
</script>

<style>

</style>
