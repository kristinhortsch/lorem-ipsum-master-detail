<template>
  <section v-if="ipsum">
    <h3>{{ ipsum.title }}</h3>
    <p>author: {{ ipsum.author }}</p>
    <p>category: {{ ipsum.category }}</p>
    <p>body: 
      <div v-html="ipsum.body"></div></p>
  </section>
</template>

<script>
export default {
  props: {
    ipsum: Object
  }

};
</script>

<style>

</style>
