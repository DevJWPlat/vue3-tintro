<template>
    <div class="todo">
      <HeroMain
          heroimage="https://poacher.platformstaging.co.uk/wp-content/uploads/sdw2208054337-scaled.jpeg"
          herocolour="black"
          title="Lets create a plan!"
          subtitle="To do list time" text="lorem ipsom sur i dar etc..."
          />
      <ImageFullwidth />
    </div>
</template>

<script>
// @ is an alias to /src
import HeroMain from '@/components/HeroMain.vue'

export default {
  name: 'ToDoView',
  components: {
    HeroMain
    
  }
}
</script>