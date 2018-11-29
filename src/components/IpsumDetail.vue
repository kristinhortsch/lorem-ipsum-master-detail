<template>
  <section v-if="ipsum" class="detail">
  
    <div class="top">
      <h3>{{ ipsum.title }}</h3>
      <p>Author: {{ ipsum.author }}</p>
      <p>Category: {{ ipsum.category }}</p>
    </div>

    <div class="body"><span>Body of Text</span>
      <div v-html="ipsum.body" class="words"></div>
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

<style scoped>
  .detail {
    text-align: center;
    border: 3px solid gray;
  }

  .body {
    padding-top: 20px;
  }

  h3 {
    padding: 0px;
    margin: 0px;
    font-size: 2em;
    color: navy;
  }

  span {
    font-size: 1.3em;
    font-weight: bold;
    color: navy;
  }

  .top {
    border-bottom: 3px solid gray;
  }
</style>
