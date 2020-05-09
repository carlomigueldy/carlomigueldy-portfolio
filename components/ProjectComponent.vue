<template>
  <div>
    <hero-component 
      background-color="primary" 
      height="100%" 
      id="projects">
      Projects
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