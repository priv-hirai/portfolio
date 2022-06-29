<template>
  <!-- <b-container fluid>
    <b-row no-gutters class="h100">
      <b-col cols="2" class="h100"><sidebar/></b-col>
      <b-col cols="10" class="h100"><nuxt/></b-col>
    </b-row>
  </b-container> -->
  <div class="h100">
    <headerhtml/>
    <nuxt class="nuxt"/>
  </div>
</template>

<script>
import headerhtml from "~/components/header";

export default {
  components: {
    headerhtml,
  },
};
</script>
<style scoped>
.nuxt {
  margin-top: 130px;
}
</style>
