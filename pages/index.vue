<template>
  <div>
    <hero-component class="text-center">
      <v-row 
        justify="center"
        align="center">
        <v-col>
          <section class="text-center">
            <div class="carlomigueldy">{ Dy }</div>
            <div class="text-center">
              <div>I am a full stack developer based in the Philippines,</div>
              <div>primarily using Laravel for building APIs and </div>
              <div>Nuxt js for the frontend.</div>
            </div>
          </section>
        </v-col>
      </v-row>
    </hero-component>

    <hero-component>
      Hello World
    </hero-component>
  </div>
</template>

<script>
import HeroComponent from '@/components/HeroComponent'

export default {
  components: {
    HeroComponent
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@100;300;400;500;700;900&display=swap');

.carlomigueldy {
  font-family: 'Noto Sans JP', sans-serif;
  font-size: 15vh;
  font-weight: 100;
}

.mx-20 {
  margin-left: 14rem;
  margin-right: 14rem;
}
</style>