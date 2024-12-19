<template>
    <div class="buttons">
        <Header :headerText="headerTitle" :buttons="buttons" />
        <HeroMain herocolour="green" title="Check out some buttons"/>
        <div class="button-container">
      
          <BaseButton color="blue" size="medium" width="max-content" border-radius="normal" href="https://google.com" target="_blank" icon="fa-brands fa-google">Google</BaseButton>
          <BaseButton color="red" size="extralarge" border-radius="small" width="full" href="/about">About</BaseButton>
          <BaseButton color="green" size="small" border-radius="large" width="max-content" href="https://www.w3schools.com/tags/att_a_target.asp" target="_blank" icon="fa-sharp fa-solid fa-graduation-cap">W3 schools</BaseButton>
          <BaseButton color="black" size="medium" border-radius="pill" width="max-content" href="/questionare">Quiz</BaseButton>
          <BaseButton color="white" size="large" width="max-content">none</BaseButton>
        </div>
    </div>
  
  </template>
  
  <script>
  import HeroMain from '@/components/HeroMain.vue'
  import BaseButton from '@/components/Button.vue'
  import Header from '@/components/Header.vue'
  
  export default {
    name: 'ButtonView',
    components: {
        HeroMain,
        BaseButton,
        Header,
    },
    data() {
        return {
        headerTitle: 'These are buttons take a look 👀',
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
  
  <style lang="scss" scoped>
    .button-container {
      margin: 50px auto;
      display: flex;
      flex-direction: column;
      gap: 25px;
      width: 50%;
      align-items: center;
    }
  </style>