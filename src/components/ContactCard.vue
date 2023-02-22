<template>
  <v-card
    class="mx-auto contact-card rounded-0"
    @click="goToGithub"
    max-width="484"
  >
    <v-card-title> {{ props.title }} </v-card-title>
  </v-card>
</template>

<script setup lang="ts">
import { defineProps, withDefaults } from "vue";
export interface Props {
  title: string;
  link: string;
}
const props = withDefaults(defineProps<Props>(), {
  title: "Titulo",
  description: "Descrição",
  link: "Link",
});

const goToGithub = () => {
  window.open(props.link);
};
</script>

<style scoped lang="scss">
.contact-card {
  margin: 0 !important;
  background-color: rgba(15, 202, 15, 0.377);
  padding-left: 40px;
  padding-right: 40px;
  color: white;
  border: 5px solid rgb(0, 211, 0);
  cursor: pointer;
}
.contact-card:hover {
  background-color: rgba(18, 255, 18, 0.377);
  color: white;
  border: 5px solid rgb(0, 211, 0);
  cursor: pointer;
}
</style>
