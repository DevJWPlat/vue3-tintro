<template>
  <div class="home">
    <HeroMain herocolour="green" title="You're home!"
      subtitle="Welcome back" text="lorem ipsom sur i dar etc..."/>
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

export default {
  name: 'HomeView',
  components: {
    HeroMain,
    BaseButton
  }
}
</script>

<style lang="scss">
  .button-container {
    margin: 50px auto;
    display: flex;
    flex-direction: column;
    gap: 25px;
    width: 50%;
    align-items: center;
  }
</style>