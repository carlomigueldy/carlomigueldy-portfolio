<template>
  <v-app app>
    <v-app-bar 
      elevate-on-scroll
      inverted-scroll
      fixed
      dense></v-app-bar>
    
    <v-content>
      <nuxt />
    </v-content>

    <v-btn 
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