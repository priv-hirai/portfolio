<template>
  <b-container fluid>
    <b-row no-gutters class="h100">
      <b-col cols="2" class="h100"><sidebar/></b-col>
      <b-col cols="10" class="h100"><nuxt/></b-col>
    </b-row>
  </b-container>
</template>

<script>
import sidebar from "~/components/sidebar";

export default {
  components: {
    sidebar,
  },
};
</script>
