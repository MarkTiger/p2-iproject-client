<template>
  <div class="col-10 custom-pt">
    <div class="d-flex flex-column">
      <div
        class="search-box d-flex align-items-center justify-content-center p-3"
      >
        <h1 class="font-chomsky">Covid Cases in Indonesia</h1>
      </div>
      <div class="bg-light mw-100 item-height p-2 overflow-auto">
        <div class="d-flex align-items-center justify-content-center">
          <img class="mw-100" :src="graph.image" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
  name: 'Corona',
  computed: {
    ...mapState(['graph']),
  },
  methods: {
    getGraph() {
      this.$store.dispatch('getGraph');
    },
  },
  created() {
    this.getGraph();
  },
};
</script>

<style></style>
