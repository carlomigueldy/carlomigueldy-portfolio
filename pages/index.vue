<template>
  <div>
    <LandingComponent id="landing" />

    <ProjectComponent id="projects" />

    <SkillComponent id="skills" />

    <AboutComponent id="about" />

    <ContactComponent id="contact" />

    <LinkComponent id="links" />
  </div>
</template>

<script>
import LandingComponent from '@/components/LandingComponent'
import SkillComponent from '@/components/SkillComponent'
import ContactComponent from '@/components/ContactComponent'
import ProjectComponent from '@/components/ProjectComponent'
import AboutComponent from '@/components/AboutComponent'
import LinkComponent from '@/components/LinkComponent'

export default {
  components: {
    LandingComponent,
    SkillComponent,
    ContactComponent,
    ProjectComponent,
    AboutComponent,
    LinkComponent
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@100;300;400;500;700;900&display=swap');

.carlomigueldy {
  font-family: 'Noto Sans JP', sans-serif;
  font-size: 15vh;
  font-weight: 300;
}

.mx-20 {
  margin-left: 14rem;
  margin-right: 14rem;
}

.parallax {
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>