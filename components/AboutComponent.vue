<template>
  <div>
    <hero-component background-color="primary" height="50vh" id="about">
      <v-row>
        <v-col 
          lg="3"
          md="3"
          sm="12"
          cols="12">
          <div class="text-center">
            <v-avatar size="64">
              <v-img src="/me.jpg"></v-img>
            </v-avatar>
          </div>
        </v-col>
        <v-col 
          lg="9"
          md="9"
          sm="12"
          cols="12">
          <v-card-text class="headline">
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
}
</script>