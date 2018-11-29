<template>
  <form @submit.prevent="onAdd(ipsum)">
    <label>
      <span>Name:</span>
      <input v-model="ipsum.title" required>
    </label>
    <label>
      <span></span>
      <button type="submit">Add</button>
      <button type="button" @click="onCancel">Cancel</button>
    </label>
  </form>
</template>

<script>
export default {
  props: {
    onAdd: Function,
    ipsum: Object
  }

};
</script>

<style>

</style>
