<template>
  <div class="app-bg">
    <div class="animation-wrapper">
      <div class="particle particle-1"></div>
      <div class="particle particle-2"></div>
      <div class="particle particle-3"></div>
      <div class="particle particle-4"></div>
    </div>

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
            <p class="title-profile mt-12">Olá,</p>
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

export default Vue.extend({});
</script>

<style scoped lang="scss">
.img-profile img {
  position: absolute;
  z-index: 1;
  border-radius: 50%;
  border: green 2px solid;
}
.title-profile {
  font-size: 45px;
  color: rgb(8, 228, 8);
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
/* Config */
$color-bg: #1e1e1e;
$color-particle: #fff;
$spacing: 2560px;
$time-1: 60s;
$time-2: 120s;
$time-3: 180s;
$time-4: 200s;

/* mixins */
@function particles($max) {
  $val: 0px 0px $color-particle;
  @for $i from 1 through $max {
    $val: #{$val}, random($spacing) + px random($spacing) + px $color-particle;
  }
  @return $val;
}

@mixin particles($max) {
  box-shadow: particles($max);
  border-radius: 50%;
}

/* Styles */
html,
body {
  height: 100%;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 4rem;
  overflow: hidden;
}

.page-bg,
.animation-wrapper {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.page-bg {
  background: $color-bg;
  background-blend-mode: screen;
  background-size: cover;
  filter: grayscale(100%);
  z-index: -1;
}

.particle,
.particle:after {
  background: transparent;
}

.particle:after {
  position: absolute;
  content: "";
  top: $spacing;
}

.particle-1 {
  animation: animParticle $time-1 linear infinite;
  @include particles(1000);
  height: 2px;
  width: 2px;
}

.particle-1:after {
  @include particles(900);
  height: 2px;
  width: 2px;
}

.particle-2 {
  animation: animParticle $time-2 linear infinite;
  @include particles(800);
  height: 2px;
  width: 2px;
}

.particle-2:after {
  @include particles(500);
  height: 3px;
  width: 3px;
}

.particle-3:after {
  @include particles(1100);
  height: 3px;
  width: 3px;
  border-radius: 50%;
}

.particle-4 {
  animation: animParticle $time-4 linear infinite;
  @include particles(1200);
  height: 1px;
  width: 1px;
}

.particle-4:after {
  @include particles(700);
  height: 1px;
  width: 1px;
}

@keyframes animParticle {
  from {
    transform: translateY(0px);
  }
  to {
    transform: translateY($spacing * -1);
  }
}

.page-wrapper {
  text-align: center;
  color: #fff;
  z-index: 2;
}

h4 {
  color: #fff;
  font-family: Monoton;
  -webkit-animation: neon1 1.5s ease-in-out infinite alternate;
  -moz-animation: neon1 1.5s ease-in-out infinite alternate;
  animation: neon1 1.5s ease-in-out infinite alternate;
}

h4:hover {
  color: #ff1177;
  -webkit-animation: none;
  -moz-animation: none;
  animation: none;
}

/*glow for webkit*/

@-webkit-keyframes neon1 {
  from {
    text-shadow: 0 0 10px #fff, 0 0 20px #fff, 0 0 30px #fff, 0 0 40px #ff1177,
      0 0 70px #ff1177, 0 0 80px #ff1177, 0 0 100px #ff1177, 0 0 150px #ff1177;
  }
  to {
    text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px #fff, 0 0 20px #ff1177,
      0 0 35px #ff1177, 0 0 40px #ff1177, 0 0 50px #ff1177, 0 0 75px #ff1177;
  }
}

/*glow for mozilla*/

@-moz-keyframes neon1 {
  from {
    text-shadow: 0 0 10px #fff, 0 0 20px #fff, 0 0 30px #fff, 0 0 40px #ff1177,
      0 0 70px #ff1177, 0 0 80px #ff1177, 0 0 100px #ff1177, 0 0 150px #ff1177;
  }
  to {
    text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px #fff, 0 0 20px #ff1177,
      0 0 35px #ff1177, 0 0 40px #ff1177, 0 0 50px #ff1177, 0 0 75px #ff1177;
  }
}

/*glow*/

@keyframes neon1 {
  from {
    text-shadow: 0 0 10px #fff, 0 0 20px #fff, 0 0 30px #fff, 0 0 40px #ff1177,
      0 0 70px #ff1177, 0 0 80px #ff1177, 0 0 100px #ff1177, 0 0 150px #ff1177;
  }
  to {
    text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px #fff, 0 0 20px #ff1177,
      0 0 35px #ff1177, 0 0 40px #ff1177, 0 0 50px #ff1177, 0 0 75px #ff1177;
  }
}
</style>
