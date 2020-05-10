<template>
  <div>
    <hero-component 
      background-color="primary" 
      height="100%">
      <h1 class="text-center mb-10">Projects</h1>
      <v-timeline>
        <v-timeline-item
          v-for="(item, i) in projects"
          :color="item.color"
          :key="i"
          small>
          <v-card 
            @click="goTo(item.link)" 
            class="elevation-2">
            <v-card-title 
              class="headline"
              v-text="item.title"
            ></v-card-title>
            <v-card-text
              v-text="item.description"
            ></v-card-text>
            <v-card-text>
              <v-chip 
                class="mr-1 mb-1"
                :key="i"
                v-for="(tech, i) in item.tech_used">
                {{ tech.name }}
                <v-icon 
                  small 
                  right 
                  v-text="tech.icon"
                ></v-icon>
              </v-chip>
            </v-card-text>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </hero-component>
  </div>
</template>

<script>
import HeroComponent from '@/components/HeroComponent'

export default {
  components: {
    HeroComponent,
  },

  methods: {
    goTo(link) {
      window.open(link, '_blank')
    }
  },

  data: () => ({
    projects: [
      {
        title: "CRM",
        color: "blue",
        date: "April 2020",
        demo_available: true,
        link: "https://fpv-crm.netlify.app/",
        description: "A custom tailored CRM System on a decoupled architecture built with Laravel 6 as the API and Nuxt js with Vuetify on the frontend.",
        tech_used: [
          {
            name: "Laravel",
            icon: "mdi-laravel"
          },
          {
            name: "Nuxt js",
            icon: "mdi-nuxt"
          },
          {
            name: "Vue js",
            icon: "mdi-vuejs"
          },
          {
            name: "Vuetify",
            icon: "mdi-vuetify"
          },
          {
            name: "Google Maps",
            icon: "mdi-google-maps"
          }
        ]
      },
      
      {
        title: "IndiGIS",
        color: "red",
        date: "November 2019",
        demo_available: true,
        link: "http://ethnogis.herokuapp.com/",
        description: "An undergraduate Capstone project, a web-based application that focuses on displaying data-driven interactive maps. It delivers data management for maintaining information, provides data visualizations using interactive driven maps and the utilization of charts of the Indigenous Groups in Northern Mindanao (Region X), Philippines. IndiGIS is built with Laravel, Vue js, Vuetify and Leaflet js. And it also integrates with the Progressive Web Application (PWA) built on Vuetify and Vue js to achieve offline data gathering capabilities.",
        tech_used: [
          {
            name: "Laravel",
            icon: "mdi-laravel"
          },
          {
            name: "Vue js",
            icon: "mdi-vuejs"
          },
          {
            name: "Vuetify",
            icon: "mdi-vuetify"
          },
          {
            name: "Leaflet",
            icon: "mdi-leaf"
          }
        ]
      },

      {
        title: "Cleaner Marawi",
        color: "green",
        date: "October 2019",
        demo_available: true,
        link: "https://dymotherhackers.firebaseapp.com/",
        description: `A prototype produced from a Hackathon named "Clean Tech Hack", it is Progressive Web Application that uses Geographical Information System with Photogrammetry for 3D modelling. Developers and Engineers for Marawi city can easily inspect what's the current state of the area and see its progress of rebuildig Marawi. This Progressive Web Application (PWA) was built with Vue js & Vuetify.`,
        tech_used: [
          {
            name: "Vue js",
            icon: "mdi-vuejs"
          },
          {
            name: "Vuetify",
            icon: "mdi-vuetify"
          },
          {
            name: "Leaflet",
            icon: "mdi-leaf"
          }
        ]
      },

      {
        title: "ASEAN Blog Entry on Sustainability",
        color: "purple",
        date: "October 2019",
        demo_available: true,
        link: "https://aseanmsuiit.firebaseapp.com/",
        description: "A simple blog on climate change prevention built with Vue js & Buefy/Bulma.",
        tech_used: [
          {
            name: "Vue js",
            icon: "mdi-vuejs"
          },
          {
            name: "Bulma",
            icon: "mdi-bulma"
          },
        ]
      },

      {
        title: "Game of Luck",
        color: "red",
        date: "August 2019",
        demo_available: true,
        link: "https://carlomigueldy.github.io/gameofluck/",
        description: "A simple game on player versus monster built with Vue js.",
        tech_used: [
          {
            name: "Vue js",
            icon: "mdi-vuejs"
          },
          {
            name: "Bootstrap",
            icon: "mdi-bootstrap"
          }
        ]
      }
    ]
  })
}
</script>
