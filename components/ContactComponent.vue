<template>
  <div>
    <hero-component 
      height="50vh" 
      id="contact">
      <div class="text-center">
        <div>
          You can contact me at
          <v-icon right>mdi-email-outline</v-icon>
        </div>
        <h1 class="display-1">
          <a href="mailto:carlomigueldy@gmail.com" style="text-decoration: none; color: #fff">carlomigueldy@gmail.com</a>
        </h1>
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