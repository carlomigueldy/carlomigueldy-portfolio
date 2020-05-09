<template>
  <div>
    <hero-component background-color="primary" height="30vh" id="links">
      <div class="text-center">
        <div class="headline">Follow Me</div>
        <v-btn depressed fab>
          <v-icon>mdi-github</v-icon>
        </v-btn>
        <v-btn depressed fab>
          <v-icon>mdi-linkedin</v-icon>
        </v-btn>
        <v-btn depressed fab>
          <v-icon>mdi-twitter</v-icon>
        </v-btn>
        <v-btn depressed fab>
          <v-icon>mdi-facebook</v-icon>
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