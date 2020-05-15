<template>
  <div>
    <hero-component height="50vh">
      <v-row>
        <v-col>
          <div class="text-center mb-10">
            <div>
              You can contact me at
              <v-icon right>mdi-email-outline</v-icon>
            </div>
            <h1 class="display-1">
              <a href="mailto:carlomigueldy@gmail.com" style="text-decoration: none; color: #fff">carlomigueldy@gmail.com</a>
            </h1>
          </div>
        </v-col>
      </v-row>
      <v-row
        v-if="false"
        justify="center"
        align="center">
        <v-col
          lg="6"
          md="6"
          sm="12"
          cols="12">
          <div class="text-center">
            <v-form action="mailto:carlomigueldy@gmail.com">
              <v-text-field
                type="text"
                name="name"
                id="name"
                label="Your name"
                hint="John Doe"
                persistent-hint
                solo
              ></v-text-field>
              <v-text-field
                type="email"
                name="email"
                id="email"
                label="Your email address"
                hint="john.doe@gmail.com"
                append-icon="mdi-email-outline"
                persistent-hint
                solo
              ></v-text-field>
              <v-textarea
                name="message"
                id="message"
                label="Your message"
                hint="Want me to build up a custom web app for your business? Let me know"
                persistent-hint
                solo
              ></v-textarea>

              <v-btn 
                color="primary"
                class="mt-10" 
                type="submit" 
                x-large>
                Send me a message
              </v-btn>
            </v-form>
          </div>
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