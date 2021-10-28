<template>
  <b-container fluid class="holder">
    <b-col cols="12" class="mNav d-block d-lg-none d-xl-none d-md-block w-100">
      <lFrame-Nav />
    </b-col>
    <b-row>
      <Frame-Left />
      <Cont-Home />
    </b-row>
  </b-container>
</template>

<style>
  @import url(./style/Frame.css);

  .holder {
    width: 100%;
    margin: 0;
    padding: 0;
  }
</style>

<script lang="ts">
  import Vue from 'vue'

  export default Vue.extend({})
</script>
