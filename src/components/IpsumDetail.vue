<template>
  <section v-if="ipsum" class="detail">
    <div class="top">
      <h3>{{ ipsum.title }}</h3>
      <p>Author: {{ ipsum.author }}</p>
      <p>Category: {{ ipsum.category }}</p>
    </div>
    <div class="body">Body of Text
      <div v-html="ipsum.body"></div>
    </div>
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
  .detail {
    text-align: center;
    border: 3px solid gray;
  }
  .body {
    padding-top: 20px;
  }
  .top {
    border-bottom: 3px solid gray;
  }

</style>
