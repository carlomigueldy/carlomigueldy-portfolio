<template>
  <div>
    <hero-component 
      background-color="primary" 
      height="50vh">
      <div class="text-center">
        <div class="mb-10">
          <span class="headline">
            by <b>Carlo Miguel Dy</b>
          </span>
          <div>
            <small>{{ '(C) ' + new Date().getFullYear() }}. All rights reserved.</small>
          </div>
        </div>
        <v-btn 
          href="https://github.com/carlomigueldy"
          target="_blank"
          depressed 
          fab>
          <v-icon large>mdi-github</v-icon>
        </v-btn>
        <v-btn 
          href="https://www.linkedin.com/in/carlo-miguel-dy-168797181/"
          target="_blank"
          depressed 
          fab>
          <v-icon large>mdi-linkedin</v-icon>
        </v-btn>
        <v-btn 
          href="https://www.instagram.com/carlomigueldy/"
          target="_blank"
          depressed 
          fab>
          <v-icon large>mdi-instagram</v-icon>
        </v-btn>
        <v-btn 
          href="https://twitter.com/CarloMiguelDy"
          target="_blank"
          depressed 
          fab>
          <v-icon large>mdi-twitter</v-icon>
        </v-btn>
        <v-btn 
          href="https://www.facebook.com/polarixdy"
          target="_blank"
          depressed 
          fab>
          <v-icon large>mdi-facebook</v-icon>
        </v-btn>
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
}
</script>