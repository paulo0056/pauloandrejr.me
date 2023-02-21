<template>
  <v-card class="mx-auto project-card" max-width="344">
    <v-img src="../assets/repo-img.png" height="200px" cover></v-img>
    <v-card-title> {{ props.title }} </v-card-title>

    <v-card-subtitle style="color: white">
      {{ props.description }}
    </v-card-subtitle>

    <v-card-actions>
      <v-btn color="orange-lighten-2" small variant="text" @click="goToGithub">
        Explore
      </v-btn>
      <v-btn
        v-if="props.isVue"
        class="tag-tech"
        small
        color="green"
        variant="text"
      >
        VUE JS
      </v-btn>
      <v-btn
        v-if="props.isTypescript"
        class="tag-tech"
        color="blue"
        small
        variant="text"
      >
        Typescript
      </v-btn>
      <v-btn
        v-if="props.isHtml"
        class="tag-tech"
        small
        color="orange"
        variant="text"
      >
        HTML
      </v-btn>
      <v-btn
        v-if="props.isCss"
        class="tag-tech"
        small
        color="pink"
        variant="text"
      >
        CSS
      </v-btn>
      <v-btn
        v-if="props.isJavascript"
        class="tag-tech"
        color="yellow"
        variant="text"
        small
      >
        Javascript
      </v-btn>
      <v-btn
        v-if="props.isNode"
        class="tag-tech"
        small
        color="#FFF59D"
        variant="text"
      >
        NODE
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script setup lang="ts">
import { ref, defineProps, withDefaults } from "vue";
export interface Props {
  title: string;
  description?: string;
  link: string;
  isVue?: boolean;
  isTypescript?: boolean;
  isHtml?: boolean;
  isNode?: boolean;
  isCss?: boolean;
  isJavascript?: boolean;
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
.tag-tech {
  cursor: auto;
}
</style>
