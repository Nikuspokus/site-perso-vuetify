<template>
  <div id="app">
    <v-app>
      <v-app-bar
        app
        color="#21222e"
        height="100"
        class="design mx-auto"
        id="home"
      >
        <v-avatar class="mr-3" size="70" @click="$vuetify.goTo('#home')">
          <v-img contain max-height="100%" src="@/assets/logo-nm.png"></v-img>
        </v-avatar>
        <v-spacer></v-spacer>

        <v-btn
          class="navbar-menu"
          style="color: #ffffff"
          text
          @click="$vuetify.goTo('#about-me')"
          >A propos de moi</v-btn
        >
        <v-btn
          style="color: #ffffff"
          text
          @click="$vuetify.goTo('#competences')"
          >Mes compétences</v-btn
        >
        <v-btn style="color: #ffffff" text @click="$vuetify.goTo('#projets')"
          >Mes projets</v-btn
        >
        <v-btn style="color: #ffffff" text @click="$vuetify.goTo('#contact')"
          >Contact</v-btn
        >
        
      </v-app-bar>

      <v-navigation-drawer
      v-model="drawer"
      absolute
      bottom
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>Foo</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Bar</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Fizz</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Buzz</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

      <section id="home">
        <v-parallax
          :height="$vuetify.breakpoint.smAndDown ? 800 : 700"
          src="@/assets/wallpaper.png"
        >
          <v-container fill-height>
            <v-row center class="white--text mx-auto" justify="center">
              <v-col class="white--text text-center" cols="12" tag="h1">
                <span
                  :class="[
                    $vuetify.breakpoint.smAndDown ? 'display-3' : 'display-4',
                  ]"
                  class="font-weight-black"
                >
                  Nicolas Marquillier
                </span>
                <br />
                <span
                  :class="[
                    $vuetify.breakpoint.smAndDown ? 'display-1' : 'display-2',
                  ]"
                  class="font-weight-light"
                >
                  Développeur Frontend, Designer
                </span>
              </v-col>
              <v-btn
                color="white"
                class="align-self-end"
                fab
                outlined
                @click="$vuetify.goTo('#about-me')"
              >
                <v-icon color="white">mdi-chevron-double-down</v-icon>
              </v-btn>
            </v-row>
          </v-container>
        </v-parallax>
      </section>
      <section id="about-me" class="design">
        <div class="py-12"></div>
        <v-container class="text-center">
          <h2 class="display-2 font-weight-bold mb-3" style="color: #ffffff">
            A PROPOS DE MOI
          </h2>
          <v-responsive class="mx-auto mb-12" max-width="150" left>
            <div
              class="title_component"
              style="
                position: relative;
                background-color: #00c3af;
                height: 5px;
                border-radius: 10px;
                z-index: 1;
              "
            ></div>
          </v-responsive>
          <v-responsive
            class="mx-auto my-9 title font-weight-light mb-8 design-text"
            max-width="720"
            style="color: #ffffff"
          >
            "Je suis passionné par le secteur du web et du design.<br />

            Après plusieurs années dans l'infographie, j'ai acquis des
            compétences de développeur Frontend.
            Je suis un développeur autodidacte."
          </v-responsive>
          <div class="mb-12 ratio">
            <v-img src="@/assets/photo_profil-2.png"></v-img>
          </div>
          <v-btn
            color="grey"
            href="cv_nicolas_marquillier.pdf"
            download
            outlined
            large
          >
            <span class="white--text text--darken-1 font-weight-bold download">
              Télécharger mon CV
            </span>
          </v-btn>
        </v-container>

        <div class="py-12"></div>
      </section>
      <section id="competences">
        <div class="py-12"></div>
        <v-container>
          <h2
            class="display-2 font-weight-bold mb-3 text-uppercase text-center"
          >
            Mes Compétences
          </h2>
          <v-responsive class="mx-auto mb-12" max-width="150" left>
            <div
              class="title_component"
              style="
                position: relative;
                background-color: #00c3af;
                height: 5px;
                border-radius: 10px;
                z-index: 1;
              "
            ></div>
          </v-responsive>
          <div class="main center">
            <div class="d-flex icone">
              <div class="competence">
                <v-img
                  src="@/assets/vuejs_logo.png"
                  center
                  style="max-width: 100px; max-height: 100px"
                ></v-img>
              </div>
              <div class="competence">
                <v-img
                  src="@/assets/groupe_5.png"
                  style="max-width: 100px; max-height: 100px"
                ></v-img>
              </div>
              <div class="competence">
                <v-img
                  src="@/assets/groupe_11.png"
                  style="max-width: 100px; max-height: 100px"
                ></v-img>
              </div>
              <div class="competence">
                <v-img
                  src="@/assets/groupe_12.png"
                  style="max-width: 100px; max-height: 100px"
                ></v-img>
              </div>
              <div class="competence">
                <v-img
                  src="@/assets/groupe_7.png"
                  style="max-width: 100px; max-height: 100px"
                ></v-img>
              </div>
              <div class="competence">
                <v-img
                  src="@/assets/groupe_6.png"
                  style="max-width: 100px; max-height: 100px"
                ></v-img>
              </div>
              <div class="competence">
                <v-img
                  src="@/assets/groupe_8.png"
                  style="max-width: 100px; max-height: 100px"
                ></v-img>
              </div>
              <div class="competence">
                <v-img
                  src="@/assets/apple_logo.png"
                  style="max-width: 100px; max-height: 100px"
                ></v-img>
              </div>
              <div class="competence">
                <v-img
                  src="@/assets/ae_logo_circle.png"
                  style="max-width: 100px; max-height: 100px"
                ></v-img>
              </div>
              <div class="competence">
                <v-img
                  src="@/assets/ai_logo_circle.png"
                  style="max-width: 100px; max-height: 100px"
                ></v-img>
              </div>
              <div class="competence">
                <v-img
                  src="@/assets/xd_logo_circle.png"
                  style="max-width: 100px; max-height: 100px"
                ></v-img>
              </div>
            </div>
          </div>
        </v-container>
        <div class="py-12"></div>
      </section>

      <section id="projets" class="design">
        <div class="py-12"></div>
        <v-container>
          <h2
            class="display-2 font-weight-bold mb-3 text-uppercase text-center"
            style="color: #ffffff"
          >
            Mes Projets
          </h2>
          <v-responsive class="mx-auto mb-12" max-width="150" left>
            <div
              class="title_component"
              style="
                position: relative;
                background-color: #00c3af;
                height: 5px;
                border-radius: 10px;
                z-index: 1;
              "
            ></div>
          </v-responsive>
          <v-row>
            <v-col
              v-for="({ text, title, time, techno }, i) in articles"
              :key="i"
              cols="12"
              md="4"
            >
              <v-card
                hover
                elevation="1"
                class="card-project"
                style="width: auto; height: 370px; border-radius: 30px"
              >
                <div>
                  <v-img
                    :src="techno"
                    height="170"
                    max-width="100%"
                    style="border-radius: 30px 30px 0px 0px"
                  >
                  </v-img>
                </div>
                <div>
                  <v-row>
                    <v-card-title
                      primary-title
                      class="justify-center"
                      style="font-size: 1.1em; margin: auto"
                    >
                      <div
                        style="width: auto; margin-top: 10px"
                        class="justify-center"
                      >
                        <h3
                          class="headline pink--text text--accent-2 text-center"
                          v-text="title"
                        ></h3>
                        <div v-text="time"></div>
                      </div>
                    </v-card-title>
                    <v-card-text
                      class="subtitle-1"
                      v-text="text"
                      style="margin: 20px; font-size: 0.9rem"
                    >
                    </v-card-text>
                    <div class="justify-content:center;"></div>
                  </v-row>
                </div>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
        <div class="py-12"></div>
      </section>
      <section id="contact">
        <div class="main center design">
          <div class="icon center">
            <a
              target="_blank"
              href="https://www.linkedin.com/in/nicolas-marquillier-aa08a4101"
            >
              <v-img
                src="@/assets/linkedin-in.svg"
                style="
                  max-width: 17px;
                  max-height: auto;
                  filter: brightness(0) invert(1);
                "
              ></v-img>
            </a>
          </div>

          <div class="icon center">
            <a target="_blank" href="mailto:nicolas.marquillier.pro@gmail.com">
              <v-img
                src="@/assets/envelope-solid.svg"
                style="
                  max-width: 17px;
                  max-height: auto;
                  filter: brightness(0) invert(1);
                "
              ></v-img>
            </a>
          </div>
        </div>
      </section>
      <v-footer
        class="justify-center"
        height="100"
        style="background-color: rgb(48, 49, 68)"
      >
        <div
          class="title font-weight-light grey--text text--lighten-1 text-center"
        >
          &copy; {{ new Date().getFullYear() }} —Made with 💚 by Nicolas
          Marquillier
        </div>
      </v-footer>
    </v-app>
  </div>
</template>

<script>
export default {
  data() {
    return {
      articles: [
        {
          title: "ARBS",
          time: "12/2020 - 02/2021",
          text:
            "Développement de l'interface selon le CDC, plateforme d'achat revente de manuel scolaire.",
          techno: require("@/assets/projet_arbs.png"),
        },
        {
          title: "Skillosi",
          time: "12/2020 - 02/2021",
          techno: require("@/assets/projet_skillosi.png"),
          text:
            "Proposition design et Développement de l'interface, plateforme de gestion de compétences internes",
        },
        {
          title: "Promod",
          time: "12/2020 - 02/2021",
          techno: require("@/assets/projet_promod_mrf.png"),
          text:
            "Réalisation de divers maquettes Adobe XD, développement d'une WebView",
        },
        {
          title: "CEF",
          time: "12/2020 - 02/2021",
          techno: require("@/assets/projet_cef.png"),
          text:
            "Développement de l'interface selon le CDC, organisme d'allocations familiales complémentaires.",
        },
        {
          title: "Rabot dutilleul",
          time: "12/2020 - 02/2021",
          techno: require("@/assets/projet_talent.png"),
          text:
            "Design et élaboration charte graphique, plateforme de mise à disposition de ressources humaines secteur BTP",
        },
        {
          title: "Carter-Cash",
          time: "12/2020 - 02/2021",
          techno: require("@/assets/projet_carter_cash.png"),
          text:
            "Proposition d'une maquette xd, pour la refonte du site en responsive",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/globals.scss";

.design {
  background-color: rgb(48, 49, 68);
}

.design-text {
  color: #ffffff;
}

.ratio {
  width: 300px;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.rounded-card {
  border-radius: 50px;
}

.main {
  height: 100;
}

.icon {
  width: 50px;
  height: 50px;
  margin: 20px;
  cursor: pointer;
  border-radius: 50px;
  transition: all 0.4s;
}

.center {
  display: flex;
  justify-content: center;
  align-items: center;
}
/*======> Gestion Contact <====== DEBUT */
.icon:nth-child(1):hover {
  box-shadow: 0 0 0 2px #00c3af;
}

.icon:nth-child(2):hover {
  box-shadow: 0 0 0 2px #00c3af;
}

.fa-linkedin-in {
  color: #fff;
  filter: drop-shadow(0 0 10px #fff);
}

.fa-coffee {
  color: #fff;
  filter: drop-shadow(0 0 10px #fff);
}
/*======> Gestion Contact <====== FIN */
.picto {
  float: left;
  width: 20px;
  height: 20px;
  margin: 20px;
  border-radius: 50px;
}

.icone {
  justify-content: center;
  flex-wrap: wrap;
}

/* COMPETENCES */
.competence:hover {
  box-shadow: 0 0 0 3px #00c3af;
  border-radius: 50px;
}

.competence {
  margin: 10px;
}

/* .jobDate {
      text-align: center;
    } */

/* .card-project {
      height: 350px;
      border-radius: 20px;
    }
    .card-project:hover {
      border: 2px solid #00C3AF;
    } */

@media (max-width: 600px) {
  .ratio {
    width: 200px;
  }

  .card-project {
    height: 50px;
    border-radius: 20px;
  }
}
</style>