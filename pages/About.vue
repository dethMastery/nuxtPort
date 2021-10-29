<template>
  <b-container fluid class="holder">
    <b-row>
      <b-col cols="12" class="mNav d-block d-lg-none d-xl-none d-md-block w-100">
        <lFrame-Nav />
      </b-col>
      <Frame-Left />
      <ContAbout />
    </b-row>
  </b-container>
</template>

<style>
  @import url(./style/Frame.css);
  @import url(./style/About.css);
</style>

<script lang="ts">
  import Vue from 'vue'
  import ContAbout from '~/components/Cont-About.vue'

  export default Vue.extend({ components: { ContAbout } })
</script>
