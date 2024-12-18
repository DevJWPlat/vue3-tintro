<template>
  <div class="about" >
    <HeroMain herocolour="blue" title="You've reached about us!"
      subtitle="Find out more here" text="lorem ipsom sur i dar etc..."/>
  </div>
</template>

<script>
// @ is an alias to /src
import HeroMain from '@/components/HeroMain.vue'

export default {
  name: 'HomeView',
  components: {
    HeroMain
  }
}
</script>
