<template>
  <v-app>
    <portfolio-home></portfolio-home>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from "vue";
import PortfolioHome from "./views/PortfolioHome.vue";

export default Vue.extend({
  name: "App",
  components: {
    PortfolioHome,
  },

  data: () => ({
    //
  }),
});
</script>
<style></style>
