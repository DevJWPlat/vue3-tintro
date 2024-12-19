<template>
  <div class="about" >
    <Header :headerText="headerTitle" :buttons="buttons" />
    <HeroMain herocolour="blue" title="You've reached about us!"
      subtitle="Find out more here" text="lorem ipsom sur i dar etc..."/>
  </div>
</template>

<script>
// @ is an alias to /src
import HeroMain from '@/components/HeroMain.vue'
import Header from '@/components/Header.vue'

export default {
  name: 'HomeView',
  components: {
    HeroMain,
    Header,
  },
  data() {
    return {
      headerTitle: 'Welcome to the About page',
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
          label: "Danger don't click",
          color: 'red',
          size: 'small',
          href: '',
          target: '_self',
          icon: 'fas fa-info-circle',
          onClick: () => alert('Self destruction countdown has begun. 3,2,1... BANG'),
        },
      ],
    };
  }
}
</script>
