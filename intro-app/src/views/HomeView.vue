<template>
  <div class="home">
    <Header :headerText="headerTitle" :buttons="buttons" />
    <HeroMain herocolour="green" title="You're home!"
      subtitle="Welcome back" text="lorem ipsom sur i dar etc..."/>
  </div>
</template>

<script>
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
      headerTitle: 'Welcome to the Home page',
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

<style lang="scss">

</style>