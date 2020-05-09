<template>
  <div>
    <hero-component 
      background-color="primary" 
      height="100%" 
      id="about">
      <v-row>
        <v-col 
          lg="3"
          md="3"
          sm="12"
          cols="12">
          <div class="text-center">
            <v-avatar class="elevation-5" size="128">
              <v-img :src="me">
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
            </v-avatar>
          </div>
        </v-col>
        <v-col 
          lg="9"
          md="9"
          sm="12"
          cols="12">
          <v-card-text>
            I am passionate in Software Engineering. I am proficient in using Javascript, PHP, SQL, leveraging on frameworks like Laravel, and Nuxt js. I also have a background in Software Engineering, Project Management, Database Security, Administration and Management, Distributed Databases, Information Engineering, and Web Services.
          </v-card-text>
        </v-col>
      </v-row>
    </hero-component>
  </div>
</template>

<script>
import HeroComponent from '@/components/HeroComponent'

export default {
  components: {
    HeroComponent,
  },

  data: () => ({
    me: '/img/me.jpg'
  })
}
</script>