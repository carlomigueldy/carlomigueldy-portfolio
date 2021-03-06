<template>
  <div>
    <hero-component 
      background-color="primary" 
      height="100%">
      <h1 class="text-center mb-10">Projects</h1>
      <v-timeline
        :dense="$vuetify.breakpoint.sm || $vuetify.breakpoint.xs">
        <v-timeline-item
          v-for="(item, i) in projects"
          :color="item.color"
          :key="i"
          small>
          <v-card 
            @click="goTo(item.link)" 
            class="elevation-2">
            <v-card-text>
              <v-img :src="item.img">
                <template v-slot:placeholder>
                  <v-row
                    class="fill-height ma-0"
                    align="center"
                    justify="center">
                    <v-progress-circular 
                      indeterminate 
                      color="grey lighten-5"
                    ></v-progress-circular>
                  </v-row>
                </template>
              </v-img>
            </v-card-text>
            <v-card-title 
              class="headline"
              v-text="item.title"
            ></v-card-title>
            <v-card-text
              v-text="item.description"
            ></v-card-text>
            <v-card-text v-if="item.demo_credentials">
              <v-card-title>Demo Credentials</v-card-title>
              <v-list>
                <v-list-item>
                  <v-list-item-content>
                    <v-list-item-title v-text="item.demo_credentials.email"></v-list-item-title>
                    <v-list-item-subtitle>Email Address</v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item>
                  <v-list-item-content>
                    <v-list-item-title v-text="item.demo_credentials.password"></v-list-item-title>
                    <v-list-item-subtitle>Password</v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-card-text>
            <v-card-text>
              <v-chip 
                class="mr-1 mb-1"
                label
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
      <div class="text-center">
        <v-dialog 
          v-model="seeMoreDialog"
          scrollable 
          max-width="1000">
          <template v-slot:activator="{ on }">
            <v-btn 
              v-on="on"
              width="250" 
              x-large>
              See More
            </v-btn>
          </template>
          <v-card>
            <v-card-title>
              More projects I built
              <v-spacer></v-spacer>
              <v-btn 
                @click="seeMoreDialog = !seeMoreDialog"
                icon>
                <v-icon>mdi-close</v-icon>
              </v-btn>
            </v-card-title>
            <v-divider></v-divider>
            <v-card-text>
              <v-timeline
                :dense="$vuetify.breakpoint.sm || $vuetify.breakpoint.xs">
                <v-timeline-item
                  v-for="(item, i) in small_projects"
                  :color="item.color"
                  :key="i"
                  small>
                  <v-card 
                    color="primary"
                    @click="goTo(item.link)" 
                    class="elevation-2">
                    <v-card-text>
                      <v-img :src="item.img">
                        <template v-slot:placeholder>
                          <v-row
                            class="fill-height ma-0"
                            align="center"
                            justify="center">
                            <v-progress-circular 
                              indeterminate 
                              color="grey lighten-5"
                            ></v-progress-circular>
                          </v-row>
                        </template>
                      </v-img>
                    </v-card-text>
                    <v-card-title 
                      class="headline"
                      v-text="item.title"
                    ></v-card-title>
                    <v-card-subtitle
                      v-text="item.date"
                    ></v-card-subtitle>
                    <v-card-text
                      v-text="item.description"
                    ></v-card-text>
                    <v-card-text v-if="item.demo_credentials">
                      <v-card-title>Demo Credentials</v-card-title>
                      <v-list>
                        <v-list-item>
                          <v-list-item-content>
                            <v-list-item-title v-text="item.demo_credentials.email"></v-list-item-title>
                            <v-list-item-subtitle>Email Address</v-list-item-subtitle>
                          </v-list-item-content>
                        </v-list-item>
                        <v-list-item>
                          <v-list-item-content>
                            <v-list-item-title v-text="item.demo_credentials.password"></v-list-item-title>
                            <v-list-item-subtitle>Password</v-list-item-subtitle>
                          </v-list-item-content>
                        </v-list-item>
                      </v-list>
                    </v-card-text>
                    <v-card-text>
                      <v-chip 
                        class="mr-1 mb-1"
                        label
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
            </v-card-text>
          </v-card>
        </v-dialog>
      </div>
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
    seeMoreDialog: false,
    
    projects: [
      {
        title: "Daycare App",
        color: "cyan",
        date: "July 2020",
        demo_available: true,
        demo_credentials: {
          email: 'admin@admin.com',
          password: 'password'
        },
        img: "/img/daycare/laptop.png",
        link: "https://childcare-web.vercel.app/",
        description: "A daycare management software that manages daycare facilities, parents, children and employees. Capable of recording child details in a timeline and has a payment system for tracking payments within the week based on parents weekly rates.",
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
            name: "Framework7",
            icon: "mdi-language-javascript"
          }
        ]
      },
      
      {
        title: "CRM",
        color: "blue",
        date: "April 2020",
        demo_available: true,
        demo_credentials: {
          email: 'admin@admin.com',
          password: 'password'
        },
        img: "/img/fpv-crm/laptop.png",
        link: "https://fpv-crm.netlify.app/",
        description: "A custom tailored CRM System on a decoupled architecture built with Laravel 6 as the API and Nuxt js with Vuetify on the frontend. The project has features like Payroll System, Clock-in & Clock-out System, Order System, Invoicing System, User Management System, Email Templating System, & a unique Reporting System.",
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
        demo_credentials: {
          email: 'admin@admin.com',
          password: 'password'
        },
        img: "/img/ethnogis/laptop.png",
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
    ],

    small_projects: [
      {
        title: "CaliShop",
        color: "blue",
        date: "April 2020",
        demo_available: true,
        demo_credentials: {
          email: 'admin@admin.com',
          password: 'password'
        },
        img: "/img/calishop/laptop.png",
        link: "https://calishop.netlify.app/",
        description: "A side project. It is a simple e-commerce application with a shopping cart system and a payment gateway.",
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
        ]
      },
      
      {
        title: "Cleaner Marawi",
        color: "green",
        date: "October 2019",
        demo_available: true,
        img: "/img/dymotherhackers/laptop.png",
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
        img: "/img/asean/laptop.png",
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
        img: "/img/gameofluck/laptop.png",
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
