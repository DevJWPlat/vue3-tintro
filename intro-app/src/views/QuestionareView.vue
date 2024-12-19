<template>
    <div class="questionare" >
      <Header :headerText="headerTitle" :buttons="buttons" />
      <HeroMain herocolour="black" title="Questionnaire"
        subtitle="Answer questions below to complete this random questionnaire"/>
      <QuestionareMulti questionslidecolour="black" title="Question one"/>
    </div>
  </template>
  
  <script>
  // @ is an alias to /src
  import HeroMain from '@/components/HeroMain.vue'
  import QuestionareMulti from '@/components/QuestionareMulti.vue'
  import Header from '@/components/Header.vue'

  export default {
    name: 'QuestionareView',
    components: {
      HeroMain,
      Header,
      QuestionareMulti
    },
  data() {
    return {
      headerTitle: 'Are you ready for the quiz?',
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
          label: 'Hint for the quiz',
          color: 'red',
          size: 'small',
          href: '',
          target: '_self',
          icon: 'fas fa-info-circle',
          onClick: () => alert('You really thought I would help you?'),
        },
      ],
    };
  }
  }
  
  </script>