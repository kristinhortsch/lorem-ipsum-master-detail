<template>
  <ul>
    <IpsumItem v-for="ipsum in ipsums"
    :key="ipsum.title"
    :ipsum="ipsum"/>
  </ul>
</template>

<script>
import IpsumItem from './IpsumItem.vue';

export default {
  props: {
    ipsums: Array
  },
  components: {
    IpsumItem
  }

};
</script>

<style>
  ul {
    list-style-type: none;
  }

</style>
