<template>
  <section>
    <IpsumList 
      v-bind:ipsums="ipsums"
      v-bind:onSelect="handleSelect"/>
    <AddIpsum />
    <Ipsum v-bind:ipsum="selected"/>
    <p>Hi</p>
  </section>
</template>

<script>
import ipsumApi from '../ipsumApi.js';
import AddIpsum from './AddIpsum.vue';
import IpsumList from './IpsumList.vue';
import Ipsum from './Ipsum.vue';

export default {
  data() {
    return {
      ipsums: ipsumApi.getIpsums(),
      selected: null
    };
  },
  components: {
    AddIpsum,
    IpsumList,
    Ipsum
  },
  methods: {
    handleSelect(ipsum) {
      this.selected = ipsum;
      console.log('you selected an item');
    }
  }
};
</script>

<style>
  img {
    width: 100%;
    height: auto;
  }

</style>
