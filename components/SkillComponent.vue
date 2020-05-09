<template>
  <hero-component id="skills">
    <v-row>
      <v-col>
        <v-card>
          <v-card-title>
            <v-row justify="center">
              <v-icon left>mdi-tools</v-icon>
              <div>Tools</div>
            </v-row>
          </v-card-title>
        </v-card>
      </v-col>
      <v-col>
        <v-card>
          <v-card-title>
            <v-row justify="center">
              <v-icon left>mdi-language-javascript</v-icon>
              <div>Languages</div>
            </v-row>
          </v-card-title>
        </v-card>
      </v-col>
      <v-col>
        <v-card>
          <v-card-title>
            <v-row justify="center">
              <v-icon left>mdi-nuxt</v-icon>
              <div>Frameworks</div>
            </v-row>
          </v-card-title>
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
}
</script>