<template>
  <v-app app>
    <v-app-bar :color="$vuetify.theme.dark ? '#022c43' : 'white'" app flat>
      <v-toolbar-title>
        <span
          @click="
            $route.name !== 'index' ? $router.replace({ name: 'index' }) : null
          "
          style="cursor:pointer"
        >
          { Dy }
        </span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <div>
        <v-btn @click="$router.push({ name: 'blog' })" text x-large>Blog</v-btn>
        <v-btn @click="$router.push({ name: 'projects' })" text x-large>
          Projects
        </v-btn>
        <v-btn
          v-if="
            $vuetify.breakpoint.md ||
              $vuetify.breakpoint.lg ||
              $vuetify.breakpoint.xl
          "
          href="https://twitter.com/CarloMiguelDy"
          target="_blank"
          elevation="0"
          color="transparent"
          fab
        >
          <v-icon>mdi-twitter</v-icon>
        </v-btn>
        <v-btn
          v-if="
            $vuetify.breakpoint.md ||
              $vuetify.breakpoint.lg ||
              $vuetify.breakpoint.xl
          "
          href="https://facebook.com/polarixdy"
          target="_blank"
          elevation="0"
          color="transparent"
          fab
        >
          <v-icon>mdi-facebook</v-icon>
        </v-btn>
        <v-btn
          href="https://github.com/carlomigueldy"
          target="_blank"
          elevation="0"
          color="transparent"
          fab
        >
          <v-icon>mdi-github</v-icon>
        </v-btn>
        <v-btn
          href="https://www.linkedin.com/in/carlo-miguel-dy-168797181/"
          target="_blank"
          elevation="0"
          color="transparent"
          fab
        >
          <v-icon>mdi-linkedin</v-icon>
        </v-btn>

        <v-btn
          @click="$vuetify.theme.dark = !$vuetify.theme.dark"
          elevation="0"
          color="transparent"
          fab
        >
          <v-icon v-if="$vuetify.theme.dark">mdi-white-balance-sunny</v-icon>
          <v-icon v-else>mdi-weather-night</v-icon>
        </v-btn>
      </div>
    </v-app-bar>

    <v-main
      :style="{
        'background-color': $vuetify.theme.dark ? '#022c43' : 'transparent'
      }"
      class="mt-10"
    >
      <v-container fill-height>
        <v-row justify="center" align="start" style="height: 100%;">
          <v-col xs="12" sm="11" md="8" lg="7" xl="6" style="height: 100%;">
            <v-row justify="center" align="start" no-gutters>
              <v-col cols="12" xs="12" sm="12" md="4" lg="4" xl="4">
                <div class="text-center">
                  <v-avatar height="150" width="150">
                    <v-img src="me.jpg"></v-img>
                  </v-avatar>
                </div>
              </v-col>
              <v-col cols="12" xs="12" sm="12" md="8" lg="8" xl="8">
                <div
                  :class="{
                    'text-left':
                      $vuetify.breakpoint.md ||
                      $vuetify.breakpoint.lg ||
                      $vuetify.breakpoint.xl,
                    'text-center mt-5':
                      $vuetify.breakpoint.sm || $vuetify.breakpoint.xs
                  }"
                >
                  <h1 class="display-2">Carlo Miguel Dy</h1>
                  <h2 class="my-3 body-1">
                    Software Engineer · Aspiring Software Architect
                  </h2>
                  <a
                    href="mailto:carlomigueldy@gmail.com"
                    class="primary--text text-decoration-none"
                  >
                    <v-icon color="primary">mdi-email-outline</v-icon>
                    <span>carlomigueldy@gmail.com</span>
                  </a>
                </div>
              </v-col>
            </v-row>

            <!-- <div class="my-5 d-flex justify-center align-center">
              <v-btn text x-large class="subtitle-1">About</v-btn>
              <v-btn text x-large class="subtitle-1">Skills</v-btn>
              <v-btn text x-large class="subtitle-1">Blog</v-btn>
              <v-btn text x-large class="subtitle-1">Projects</v-btn>
              <v-btn text x-large class="subtitle-1">Contact</v-btn>
            </div> -->

            <v-divider class="my-10"></v-divider>
            <Nuxt />
          </v-col>
        </v-row>
      </v-container>
    </v-main>

    <v-footer :color="$vuetify.theme.dark ? '#022c43' : 'white'">
      <v-container>
        <div class="text-center">
          Made with ❤️ by Carlo Miguel Dy
        </div>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script lang="ts">
export default {
  computed: {}
};
</script>
