<template>
  <div>
    <v-img 
      max-height="100vh" 
      src="/wallpaper.jpg"
      class="parallax"
      gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.95)">
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
      <hero-component id="landing" class="text-center">
        <v-row 
          justify="center"
          align="center">
          <v-col>
            <section class="text-center">
              <div class="carlomigueldy">{ Dy }</div>
              <div class="text-center">
                <div class="display-1 mb-5">
                  <typewriter
                    :speed="80"
                    :full-erase="true"
                    :interval="1000"
                    :repeat="true"
                    :words="[
                      'I am a full stack developer based in the Philippines',
                      'primarily using Laravel for building APIs',
                      'and Nuxt js for the frontend'
                    ]">
                  </typewriter>
                </div>
                <v-btn 
                  x-large 
                  color="primary"
                  @click="$vuetify.goTo('#projects')">
                  Projects
                  <v-icon right>mdi-chevron-down</v-icon>
                </v-btn>
              </div>
            </section>
          </v-col>
        </v-row>
      </hero-component>
    </v-img>
  </div>
</template>

<script>
import HeroComponent from '@/components/HeroComponent'

export default {
  components: {
    HeroComponent,
  },
}
</script>