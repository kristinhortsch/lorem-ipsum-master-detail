<template>
  <ul>
    <IpsumItem 
      v-for="ipsum in ipsums"
      @click.native="onSelect(ipsum)"
      :key="ipsum.title"
      :ipsum="ipsum"/>
  </ul>
</template>

<script>
import IpsumItem from './IpsumItem.vue';

export default {
  props: {
    ipsums: Array,
    onSelect: Function
  },
  components: {
    IpsumItem
  }
};
</script>

<style>
  ul {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    grid-column-gap: 10px;
    grid-row-gap: 10px;
    list-style-type: none;
    margin: 0;
    padding: 0;
  }
</style>
