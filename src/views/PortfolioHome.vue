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
        <!--  <v-col> <a> Imagem home </a></v-col> -->
        <v-col>
          <v-row justify="end" class="mr-2">
            <a href="#about" class="mt-3"> Sobre </a>
            <a href="#projects" class="mt-3"> Projetos </a>
            <a href="#contact" class="mt-3"> Contato </a>
          </v-row>
        </v-col>
      </v-row>
    </div>

    <div>
      <v-container class="main">
        <v-row justify="center">
          <p class="name-title">Paulo Andre Brito de Almeida Junior</p></v-row
        >
        <v-row id="about">
          <v-col class="hire-me-column">
            <p class="title-profile mt-12">Olá,</p>
            <p class="subtitle-profile">Eu me chamo Paulo André</p>
            <p class="description-profile">
              Sou um desenvolvedor front-end formado pela UNEB(Universidade do
              Estado da Bahia), trabalho na área de desenvolvimento há 4 anos,
              com foco no desenvolvimento front end mais especificamente com Vue
              Js, JavaScript e TypeScript com as quais trabalho atualmente na
              GWCloud. Também tive experiencia em gestão de projetos na epoca em
              que atuei como Presidente da Empresa Junior Tecno System a qual
              sou conselheiro atualmente. Sou uma pessoa que ama trabalhar em
              equipe e que tem uma fome gigantesca por adiquirir novos
              conhecimentos, desejo continuar agregando aonde quer que eu passe
              com o meu trabalho e conhecimento para que eu possa crescer
              profissionalmente cada vez mais e consiga alcançar minhas
              ambições.
            </p>
            <v-btn color="green" class="white--text mt-5">
              <a href="#contact" style="text-decoration: none; color: white">
                Me contrate
              </a></v-btn
            >
          </v-col>
        </v-row>
        <v-row class="row-custom" align="center">
          <v-col xs="12" sm="12" md="12" lg="6" xl="6">
            <v-row justify="center" align="end">
              <img
                src="../assets/js-logo.png"
                class="jsts-logo"
                alt="js-logo"
              />
              <img
                src="../assets/vue-logo3.png"
                height="250"
                max-width="250"
                style="margin-bottom: 100px"
                alt="vue-logo"
                class="vue-logo"
              />
              <img
                src="../assets/ts-logo.png"
                class="jsts-logo"
                alt="ts-logo"
              />
            </v-row>
          </v-col>
          <v-col cols="12" sm="12" md="12" lg="6" xl="6">
            <p class="title-profile mt-12">Skillset</p>

            <p class="description-profile">
              Minha stack de tecnologias atual é Html, CSS, JavaScript,
              TypeScript e Vue, mas tenho conhecimentos e projetos também na
              área de desenvolvimento com wordpress, php e react e em
              desenvolvimento mobile com o Flutter e modelagem de banco de dados
              MySQL e MongoDB.
            </p>
          </v-col>
        </v-row>
        <v-row class="row-custom exp-title">
          <v-col
            ><span style="color: white; margin-left: 20px; font-size: 35px"
              >Exp</span
            >
            <hr style="margin-left: 23px; max-width: 95%"
          /></v-col>
        </v-row>
        <v-row justify="center">
          <v-tabs
            v-model="tab"
            background-color="transparent"
            style="max-width: 1100px"
            dark
          >
            <v-tab>
              <v-row justify="start">
                <v-icon left> mdi-account </v-icon> GWCloud</v-row
              >
            </v-tab>
            <v-tab>
              <v-row justify="start">
                <v-icon left> mdi-account </v-icon> Tecno System</v-row
              >
            </v-tab>
          </v-tabs>

          <v-tabs-items v-model="tab" dark>
            <v-tab-item>
              <v-card flat class="tab-custom">
                <v-card-text style="color: white">
                  <h2>Estagiário</h2>
                  <h3
                    style="
                      color: rgb(8, 228, 8);
                      font-weight: 700;
                      font-size: 17px;
                    "
                  >
                    GWCloud
                  </h3>
                  <p style="font-size: 17px">2021</p>
                  <p style="max-width: 1100px" class="exp-description">
                    Participação das plainnings e atuando na programação
                    front-end nos sistemas web da empresa, usando javascript,
                    typescript, Vue e design patterns como DDD e TDD
                  </p>
                  <h2>Programador Junior</h2>
                  <h3
                    style="
                      color: rgb(8, 228, 8);
                      font-size: 17px;
                      font-weight: 700;
                    "
                  >
                    GWCloud
                  </h3>
                  <p style="font-size: 17px">2022-Atualmente</p>
                  <p style="max-width: 1100px" class="exp-description">
                    Participação das plainnings e atuando na programação
                    front-end nos sistemas web da empresa, usando javascript,
                    typescript, Vue e design patterns como DDD e TDD
                  </p>
                </v-card-text>
              </v-card>
            </v-tab-item>
            <v-tab-item>
              <v-card flat class="tab-custom">
                <v-card-text style="color: white">
                  <h2>Programador</h2>
                  <h3 style="color: rgb(8, 228, 8); font-weight: 700">
                    Tecno System
                  </h3>
                  <p style="font-size: 15px">2020-2021</p>

                  <p style="max-width: 1100px" class="exp-description">
                    Desenvolvimento de sites com wordpress e programação dos
                    sistemas da empresa desde a modelagem de banco de dados até
                    a programação de back end e front end com Php, react e MySql
                    , alem de participar do gerenciamento de projetos e
                    acompanhamento de trainees.
                  </p>
                  <h2>Presidente</h2>
                  <h3 style="color: rgb(8, 228, 8); font-weight: 700">
                    Tecno System
                  </h3>
                  <p style="font-size: 15px">2021-2022</p>

                  <p style="max-width: 1100px" class="exp-description">
                    Criação de planejamento estratégico, controle financeiro,
                    gestão de pessoas, atividades administrativas da empresa e
                    gerenciamento de projetos
                  </p>
                </v-card-text>
              </v-card>
            </v-tab-item>
          </v-tabs-items>
        </v-row>
        <v-row class="row-custom" id="projects">
          <v-col
            ><span style="color: white; margin-left: 20px; font-size: 35px"
              >Projetos</span
            >
            <hr style="margin-left: 23px; max-width: 95%"
          /></v-col>
        </v-row>
        <v-row>
          <v-col
            ><CardProject
              :title="'Gado na Bahia'"
              :description="'Site catalogo de vendas de gados na Bahia'"
              :link="'https://gadonabahia.com.br/'"
              :img="'gadonabahia.png'"
            ></CardProject
          ></v-col>
          <v-col
            ><CardProject
              :title="'Site Tecno System'"
              :description="'Site da empresa junior Tecno System'"
              :link="'https://tecnosystemej.com.br/'"
              :img="'tecnosystem.png'"
            ></CardProject
          ></v-col>
          <v-col
            ><CardProject
              :title="'Pokedex'"
              :description="'Uma pokedex feita com Vue js'"
              :link="'https://paulo0056.github.io/pokedex-vue3/'"
              :img="'pokedex.png'"
            ></CardProject
          ></v-col>
          <v-col
            ><CardProject
              :title="'Jogo da Memória'"
              :description="'Um jogo da memoria do anime One Piece'"
              :link="'https://paulo0056.github.io/memory-game/pages/index.html'"
              :img="'memory-game.png'"
            ></CardProject
          ></v-col>
        </v-row>
        <v-row class="row-custom repo-title">
          <v-col
            ><span style="color: white; margin-left: 20px; font-size: 35px"
              >Repos</span
            >
            <hr style="margin-left: 23px; max-width: 95%"
          /></v-col>
        </v-row>
        <v-row>
          <v-col
            ><CardRepo
              :title="'TS Node Setup'"
              :description="'Setup para projetos com Node e Typescript'"
              :link="'https://github.com/paulo0056/ts-node-setup'"
              :is-typescript="true"
              :is-node="true"
            ></CardRepo
          ></v-col>
          <v-col
            ><CardRepo
              :title="'Posts Node'"
              :description="'Repositorio para estudos com Node Js'"
              :link="'https://github.com/paulo0056/node-posts-study'"
              :is-javascript="true"
              :is-node="true"
            ></CardRepo
          ></v-col>
          <v-col
            ><CardRepo
              :title="'Clean Node API'"
              :description="'Projeto para criação de API com DDD e TDD'"
              :link="'https://github.com/paulo0056/clean-node-api'"
              :is-typescript="true"
              :is-node="true"
            ></CardRepo
          ></v-col>
          <v-col
            ><CardRepo
              :title="'User API Node'"
              :description="'Api de criação de usuarios para estudo'"
              :link="'https://github.com/paulo0056/user-api-node'"
              :is-typescript="true"
              :is-node="true"
            ></CardRepo
          ></v-col>
          <v-col
            ><CardRepo
              :title="'Pokedex'"
              :description="'Projeto pokedex repositorio'"
              :link="'https://github.com/paulo0056/pokedex-vue3'"
              :is-vue="true"
              :is-typescript="true"
              :is-css="true"
            ></CardRepo
          ></v-col>
          <v-col
            ><CardRepo
              :title="'Jogo da Memória'"
              :description="'Projeto jogo da memoria repositorio'"
              :link="'https://github.com/paulo0056/memory-game'"
              :is-html="true"
              :is-css="true"
              :is-javascript="true"
            ></CardRepo
          ></v-col>

          <v-col
            ><CardRepo
              :title="'Animação da Matrix'"
              :description="'Uma animação da matrix para background'"
              :link="'https://github.com/paulo0056/Matrix-Animation'"
              :is-html="true"
              :is-javascript="true"
              :is-css="true"
            ></CardRepo
          ></v-col>
          <v-col
            ><CardRepo
              :title="'Calculadora Js'"
              :description="'Uma calculadora em javascript'"
              :link="'https://github.com/paulo0056/Matrix-Animation'"
              :is-html="true"
              :is-css="true"
              :is-javascript="true"
            ></CardRepo
          ></v-col>

          <v-col
            ><CardRepo
              :title="'pauloandre.me'"
              :description="'Repositorio do meu site de apresentação'"
              :link="'https://github.com/paulo0056/pauloandrejr.me'"
              :is-typescript="true"
              :is-vue="true"
              :is-css="true"
            ></CardRepo
          ></v-col>
        </v-row>
        <v-row class="row-custom" id="contact">
          <v-col
            ><span style="color: white; margin-left: 20px; font-size: 35px"
              >Contato</span
            >
            <hr style="margin-left: 23px; max-width: 95%"
          /></v-col>
        </v-row>

        <v-row justify="center" style="margin-top: 30px">
          <ContactCard
            :title="'Linkedin'"
            :link="'https://www.linkedin.com/in/paulojr-dev/'"
          ></ContactCard>
          <ContactCard
            :title="'Instagram'"
            :link="'https://www.instagram.com/pauloandrejrr/'"
          ></ContactCard>
          <ContactCard
            :title="'WhatsApp'"
            :link="'https://api.whatsapp.com/send?phone=5575992909426'"
          ></ContactCard>
        </v-row>
        <v-row justify="center" style="margin-top: 30px">
          <ContactCard
            :title="'Email: pauloandre.dev@gmail.com'"
            :link="'https://mail.google.com/mail/u/0/#inbox'"
            :width="'420'"
          ></ContactCard>
        </v-row>
        <v-row justify="center" class="row-custom"
          ><span style="color: white; margin-left: 20px" class="rights-reserved"
            >© 2023 Paulo André.</span
          ></v-row
        >
        <v-row justify="center"
          ><span style="color: white; margin-left: 20px" class="rights-reserved"
            >Todos os direitos reservados.</span
          ></v-row
        >
      </v-container>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import CardRepo from "../components/CardRepo.vue";
import CardProject from "../components/CardProject.vue";
import ContactCard from "../components/ContactCard.vue";

const tab = ref<boolean>(false);
</script>

<style scoped lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Oxanium:wght@300;400;500;600;700;800&display=swap");
@import url("https://fonts.cdnfonts.com/css/karmatic-arcade");
@import url("https://fonts.cdnfonts.com/css/war-eagle-condensed");

.hire-me-column {
  margin-top: 20px;
}
.name-title {
  font-size: 50px;
  font-weight: 500;
  color: white;
  font-family: "Karmatic Arcade", sans-serif;
}

@media (max-width: 380px) {
  .rights-reserved {
    font-size: 15px;
  }
}
.theme--dark.v-icon {
  color: rgb(8, 228, 8);
}
.theme--dark.v-tabs-items {
  background-color: transparent !important;
}

.theme--light.v-tabs-items {
  background-color: transparent !important;
}
.row-custom {
  margin-top: 150px;
}

.vue-logo {
  transform: translateY(20px);
  z-index: 1;
}
.jsts-logo {
  z-index: 1;
  height: 140px;
  max-width: 140px;
  border-radius: 10px;
}
@media (max-width: 620px) {
  .vue-logo {
    transform: translateY(20px);
    height: 120px;
    max-width: 120px;
    z-index: 1;
  }
  .jsts-logo {
    z-index: 1;
    height: 70px;
    max-width: 70px;
    border-radius: 10px;
  }
}
.img-profile img {
  position: absolute;
  margin-left: 150px;
  z-index: 2;
  max-height: 50%;
  max-width: 30%;
}
#projects {
  font-family: "War Eagle", sans-serif;
}

#contact {
  font-family: "War Eagle", sans-serif;
}
.tab-custom {
  background-color: transparent !important;
}
.title-profile {
  font-size: 45px;
  color: rgb(8, 228, 8);
  font-family: "War Eagle", sans-serif;
}
.repo-title {
  font-family: "War Eagle", sans-serif;
}
.exp-description {
  font-size: 20px;
  font-weight: 400;
}
.exp-title {
  font-family: "War Eagle", sans-serif;
}
.subtitle-profile {
  font-size: 45px;
  font-family: "War Eagle Condensed", sans-serif;
  color: white;
}
.description-profile {
  font-size: 22px;

  color: white;
  font-weight: 300;
}
.app-bg {
  background-color: black;
  height: 100%;
  width: 100%;
}
.navbar {
  z-index: 1;
  overflow: hidden;
  background-color: rgba(0, 0, 0, 0.616);
  padding: 10px;
  font-size: 22px;
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

/* Main content */
.main {
  font-family: "Oxanium", cursive;
  margin-top: 100px; /* Add a top margin to avoid content overlay */
  max-width: 1640px;
  margin-left: auto;
  margin-right: auto;
  padding: 50px;
}

/* Config BG Animated*/
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
