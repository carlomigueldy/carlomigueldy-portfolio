<template>
  <v-card 
    :color="backgroundColor"
    height="100vh"
    flat
    tile>
    <v-container 
      fill-height>
      <v-row
        justify="center"
        align="center">
        <v-col
          :lg="lg"
          :md="md"
          :sm="sm"
          :cols="cols">
          <slot name="default" />
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
export default {
  props: {
    backgroundColor: {
      type: String,
      default: () => 'transparent'
    },

    lg: {
      type: String,
      default: () => '12'
    },

    md: {
      type: String,
      default: () => '12'
    },

    sm: {
      type: String,
      default: () => '12'
    },

    cols: {
      type: String,
      default: () => '12'
    },
  }
}
</script>