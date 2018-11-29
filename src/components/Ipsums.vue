<template>
  <section>
    <AddIpsum v-bind:onAdd="handleAdd"/>
    <IpsumList 
      class="list"
      v-bind:ipsums="ipsums"
      v-bind:onSelect="handleSelect"/>
    <Ipsum v-bind:ipsum="selected"/>
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
    },
    handleAdd(ipsum) {
      this.ipsums.push(ipsum);
      this.handleSelect(ipsum);
    }
  }
};
</script>

<style>
  img {
    width: 35vw;
    max-width: 250px;
    height: auto;
    display: block;
    margin: 10px auto;
    box-shadow: 2px 2px 1px black;
  }

  section {
    padding: 20px;
  }
</style>
