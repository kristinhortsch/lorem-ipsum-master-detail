<template>
  <section>
    <IpsumList v-bind:ipsums="ipsums"/>
    <AddIpsum />
    <Ipsum />
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
      ipsums: ipsumApi.getIpsums()
    };
  },
  components: {
    AddIpsum,
    IpsumList,
    Ipsum
  }
};
</script>

<style>
  img {
    width: 100%;
    height: auto;
  }

</style>
