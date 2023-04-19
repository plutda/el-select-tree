<script>
import Vue from 'vue';
import { getData } from '../src/util'
// import { Vue2SelectTreeSample } from '@/entry.esm';
import { Vue2SelectTreeSample } from '../dist/vue2-select-tree.esm';

export default Vue.extend({
  name: 'ServeDev',
  components: {
   Vue2SelectTreeSample,
  },
  data() {
    return {
      data: [],
      select: []
    }
  },
  methods: {
  },
  mounted() {
    this.data = getData()
  }
});
</script>

<template>
  <div id="app">
    <vue2-select-tree-sample
      :value.sync="select"
      :data="data"
    />
  </div>
</template>
