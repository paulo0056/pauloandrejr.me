<template>
  <div class="app-bg">
    <div class="navbar">
      <v-row justify="space-between">
        <v-col> <a> Imagem home </a></v-col>
        <v-col>
          <v-row justify="end" class="mr-2">
            <router-link to="#projects" class="mt-3"> Projetos </router-link>
            <router-link to="#about" class="mt-3"> Sobre </router-link>
            <router-link to="#contact" class="mt-3"> Contato </router-link>
          </v-row>
        </v-col>
      </v-row>
    </div>

    <div class="main">
      <v-container
        ><v-row>
          <v-col cols="6">
            <HelloUsers />
            <p class="title-profile mt-12">.</p>
            <p class="subtitle-profile">Eu sou Paulo André</p>
            <p class="description-profile">
              Eu sou um programador com mais de 4 anos de experiencia. Minha
              expertise está no desenvolvimento front-end de aplicações web.
            </p>
            <v-btn color="green" class="white--text mt-5"
              >Me contrate</v-btn
            ></v-col
          >
          <v-col cols="6">
            <div class="img-profile">
              <img src="../assets/img-teste.png" alt="profile-img" />
            </div>

            /></v-col
          >
        </v-row></v-container
      >
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import HelloUsers from "../components/HelloUsers.vue";

export default Vue.extend({
  components: {
    HelloUsers,
  },
});
</script>

<style scoped>
.img-profile img {
  border-radius: 50%;
  border: green 2px solid;
}
.title-profile {
  font-size: 45px;
  color: rgba(19, 216, 19, 0);
}
.subtitle-profile {
  font-size: 45px;
  color: white;
}
.description-profile {
  font-size: 15px;
  color: white;
  font-weight: 300;
}
.app-bg {
  background-color: black;
  height: 100%;
  width: 100%;
}
.navbar {
  overflow: hidden;
  background-color: rgba(0, 0, 0, 0.301);
  padding: 10px;
  position: fixed; /* Set the navbar to fixed position */
  top: 0; /* Position the navbar at the top of the page */
  width: 100%; /* Full width */
}

/* Links inside the navbar */
.navbar a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  font-weight: bold;
  padding: 14px 16px;
  text-decoration: none;
}

/* Change background on mouse-over */
.navbar a:hover {
  color: rgb(19, 216, 19);
}
@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");
/* Main content */
.main {
  font-family: "Roboto", sans-serif;
  margin-top: 100px; /* Add a top margin to avoid content overlay */
}
</style>
