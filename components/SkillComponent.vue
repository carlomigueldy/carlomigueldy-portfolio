<template>
  <hero-component height="100%">
    <h1 class="text-center mb-10">Here is my stack</h1>
    <v-row>
      <v-col lg="4" md="4" sm="12" cols="12">
        <v-card min-height="25rem" height="100%">
          <v-card-title>
            <v-row justify="center">
              <v-icon left>mdi-tools</v-icon>
              <div>Tools</div>
            </v-row>
          </v-card-title>
          <v-list>
            <v-list-item v-for="(item, i) in tools" :key="i">
              <v-list-item-action>
                <v-icon v-text="item.icon"></v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title v-text="item.title"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
      <v-col lg="4" md="4" sm="12" cols="12">
        <v-card min-height="25rem" height="100%">
          <v-card-title>
            <v-row justify="center">
              <v-icon left>mdi-code-braces</v-icon>
              <div>Languages</div>
            </v-row>
          </v-card-title>
          <v-list>
            <v-list-item v-for="(item, i) in languages" :key="i">
              <v-list-item-action>
                <v-icon v-text="item.icon"></v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title v-text="item.title"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
      <v-col lg="4" md="4" sm="12" cols="12">
        <v-card min-height="25rem" height="100%">
          <v-card-title>
            <v-row justify="center">
              <v-icon left>mdi-nuxt</v-icon>
              <div>Frameworks</div>
            </v-row>
          </v-card-title>
          <v-list>
            <v-list-item v-for="(item, i) in frameworks" :key="i">
              <v-list-item-action>
                <v-icon v-text="item.icon"></v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title v-text="item.title"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
    </v-row>
  </hero-component>
</template>

<script>
import HeroComponent from "@/components/HeroComponent";

export default {
  components: {
    HeroComponent,
  },

  data: () => ({
    tools: [
      {
        title: "Visual Studio Code",
        icon: "mdi-microsoft-visual-studio-code",
      },
      {
        title: "Nginx / Apache2",
        icon: "mdi-server",
      },
      {
        title: "Git",
        icon: "mdi-git",
      },
      {
        title: "Bash",
        icon: "mdi-bash",
      },
      {
        title: "Linux",
        icon: "mdi-linux",
      },
    ],

    languages: [
      {
        title: "PHP",
        icon: "mdi-language-php",
      },
      {
        title: "JavaScript",
        icon: "mdi-language-javascript",
      },
      {
        title: "TypeScript",
        icon: "mdi-language-typescript",
      },
      {
        title: "Dart",
        icon: "mdi-code-braces",
      },
      {
        title: "Python",
        icon: "mdi-language-python",
      },
    ],

    frameworks: [
      {
        title: "Laravel",
        icon: "mdi-laravel",
      },
      {
        title: "Vue",
        icon: "mdi-vuejs",
      },
      {
        title: "Angular",
        icon: "mdi-angular",
      },
      {
        title: "React",
        icon: "mdi-react",
      },
      {
        title: "Nuxt",
        icon: "mdi-nuxt",
      },
      {
        title: "Flutter",
        icon: "mdi-cellphone",
      },
    ],
  }),
};
</script>
