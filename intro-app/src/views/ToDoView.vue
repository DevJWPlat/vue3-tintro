<template>
    <div class="todo">
      <Header :headerText="headerTitle" :buttons="buttons" />
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
import Header from '@/components/Header.vue'

export default {
  name: 'ToDoView',
  components: {
    HeroMain,
    Header,
  },
  data() {
    return {
      headerTitle: 'This will be the to do list - if i ever build it',
      buttons: [
        {
          label: 'Home',
          color: 'blue',
          size: 'small',
          href: '/',
          target: '_self',
          icon: 'fas fa-home',
        },
        {
          label: 'Quiz',
          color: 'green',
          size: 'small',
          href: 'questionare',
          target: '_self',
        },
        {
          label: 'Help',
          color: 'red',
          size: 'small',
          href: '',
          target: '_self',
          icon: 'fas fa-info-circle',
          onClick: () => alert('Why have you clicked help?'),
        },
      ],
    };
  }
}
</script>