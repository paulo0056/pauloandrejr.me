<template>
  <v-card class="mx-auto project-card" max-width="344">
    <v-img src="../assets/gadonabahia.png" height="200px" cover></v-img>
    <v-card-title> {{ props.title }} </v-card-title>

    <v-card-subtitle style="color: white">
      {{ props.description }}
    </v-card-subtitle>

    <v-card-actions>
      <v-btn color="orange-lighten-2" variant="text" @click="goToGithub">
        Explore
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script setup lang="ts">
import { ref, defineProps, withDefaults } from "vue";
export interface Props {
  title: string;
  description: string;
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
.project-card {
  background-color: rgba(15, 202, 15, 0.377);
  color: white;
  border: 1px solid rgb(0, 211, 0);
}
</style>
