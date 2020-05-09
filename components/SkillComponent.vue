<template>
  <hero-component height="100%" id="skills">
    <v-row>
      <v-col
        lg="4"
        md="4"
        sm="12"
        cols="12">
        <v-card 
          min-height="25rem" 
          height="100%">
          <v-card-title>
            <v-row justify="center">
              <v-icon left>mdi-tools</v-icon>
              <div>Tools</div>
            </v-row>
          </v-card-title>
          <v-list>
            <v-list-item v-for="(item, i) in tools" :key="i">
              <v-list-item-title v-text="item.title"></v-list-item-title>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
      <v-col
        lg="4"
        md="4"
        sm="12"
        cols="12">
        <v-card 
          min-height="25rem" 
          height="100%">
          <v-card-title>
            <v-row justify="center">
              <v-icon left>mdi-language-javascript</v-icon>
              <div>Languages</div>
            </v-row>
          </v-card-title>
          <v-list>
            <v-list-item v-for="(item, i) in languages" :key="i">
              <v-list-item-title v-text="item.title"></v-list-item-title>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
      <v-col
        lg="4"
        md="4"
        sm="12"
        cols="12">
        <v-card 
          min-height="25rem" 
          height="100%">
          <v-card-title>
            <v-row justify="center">
              <v-icon left>mdi-nuxt</v-icon>
              <div>Frameworks</div>
            </v-row>
          </v-card-title>
          <v-list>
            <v-list-item v-for="(item, i) in frameworks" :key="i">
              <v-list-item-title v-text="item.title"></v-list-item-title>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
    </v-row>
  </hero-component>
</template>

<script>
import HeroComponent from '@/components/HeroComponent'

export default {
  components: {
    HeroComponent,
  },

  data: () => ({
    tools: [
      {
        title: 'Visual Studio Code',
      },
      {
        title: 'Nginx / Apache2',
      },
      {
        title: 'Git',
      },
      {
        title: 'Bash',
      },
      {
        title: 'Linux',
      },
    ],

    languages: [
      {
        title: 'JavaScript',
      },
      {
        title: 'TypeScript',
      },
      {
        title: 'Java',
      },
      {
        title: 'Python',
      },
      {
        title: 'PHP',
      },
    ],

    frameworks: [
      {
        title: 'Laravel',
      },
      {
        title: 'Vue',
      },
      {
        title: 'Nuxt',
      },
      {
        title: 'Vuetify',
      },
      {
        title: 'Angular',
      },
    ]
  })
}
</script>