<template>
  <v-app app>
    <v-app-bar 
      elevate-on-scroll
      inverted-scroll
      fixed
      dense>
      <v-spacer></v-spacer>
      <v-app-bar-nav-icon 
        @click="drawer = !drawer" 
      />
    </v-app-bar>
    
    <v-content>
      <nuxt />
    </v-content>

    <v-navigation-drawer
      v-model="drawer"
      temporary
      right
      app>
      <v-list>
        <v-list-item 
          two-line
          :key="i"
          v-for="(item, i) in elements"
          @click="$vuetify.goTo(item.id).then(() => drawer = !drawer)">
          <v-list-item-action></v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

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
  data: () => ({
    drawer: false,
    elements: [
      {
        id: '#landing',
        title: 'Main',
      },
      {
        id: '#projects',
        title: 'Projects',
      },
      {
        id: '#skills',
        title: 'Skills',
      },
      {
        id: '#about',
        title: 'About',
      },
      {
        id: '#contact',
        title: 'Contact',
      },
      {
        id: '#links',
        title: 'Links',
      },
    ]
  }),
}
</script>