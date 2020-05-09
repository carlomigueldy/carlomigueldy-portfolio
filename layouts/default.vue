<template>
  <v-app app>
    <v-app-bar 
      elevate-on-scroll
      inverted-scroll
      fixed
      dense>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-toolbar-title>Carlo Miguel Dy</v-toolbar-title>
      <v-spacer></v-spacer>
      
      <v-btn>About</v-btn>
    </v-app-bar>
    
    <v-content>
      <nuxt />
    </v-content>

    <v-btn 
      @click="$vuetify.goTo('#landing')"
      fixed 
      bottom 
      right
      fab>
      <v-icon large>mdi-chevron-up</v-icon>
    </v-btn>    
  </v-app>
</template>

<script>
export default {
  
}
</script>