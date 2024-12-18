<template>
    <div class="questionare" >
      <HeroMain herocolour="black" title="Questionnaire"
        subtitle="Answer questions below to complete this random questionnaire"/>
      <QuestionareMulti questionslidecolour="black" title="Question one"/>
    </div>
  </template>
  
  <script>
  // @ is an alias to /src
  import HeroMain from '@/components/HeroMain.vue'
  import QuestionareMulti from '@/components/QuestionareMulti.vue'
  
  export default {
    name: 'QuestionareView',
    components: {
      HeroMain,
      QuestionareMulti
    }
  }
  
  </script>