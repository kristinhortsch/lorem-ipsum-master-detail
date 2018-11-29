<template>
  <li>
    <p class="name tiles">{{ ipsum.title }}</p>
    <p class="tiles">Category: {{ ipsum.category }}</p>
  </li>
</template>

<script>
export default {
  props: {
    ipsum: Object
  }
};
</script>

<style>
  li {
    position: relative;
    height: 150px;
    border: 5px solid;
    background: black;
    border: 3px solid navy;
    padding: 10px;
    margin-bottom: 10px;
    box-shadow: 2px 2px 2px black;
  }

  .tiles {
    color: white;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    text-align: center;
  }

  .name {
    font-size: 1.5em;

  }

</style>

