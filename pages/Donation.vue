<template>
  <b-container fluid class="holder">
    <b-row>
      <b-col cols="12" class="mNav d-block d-lg-none d-xl-none d-md-block w-100">
        <lFrame-Nav />
      </b-col>
      <Frame-Left />
      <Cont-Donation />
    </b-row>
  </b-container>
</template>

<style>
  @import url(./style/Frame.css);
  @import url(./style/Donation.css);
</style>

<script lang="ts">
  import Vue from 'vue'
  
  export default Vue.extend({})
</script>
