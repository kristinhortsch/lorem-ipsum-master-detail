<template>
  <ul>
    <p>Hello from IpsumList</p>
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

</style>
