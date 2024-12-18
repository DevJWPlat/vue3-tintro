<template>
    <div class="hello" :class="herocolour">
      <img v-if="heroimage" :src="heroimage">
      <h1>{{ title }}</h1>
      <p>{{ subtitle }}</p>
      <p>{{ text }}</p>
  
    </div>
  </template>
  
  <script>
  export default {
    name: 'HeroMain',
    props: {
      title: String,
      subtitle: String,
      text: String,
      herocolour: String,
      heroimage: String
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  .blue {
      background: blue;
      padding: 50px;
      color: white;
      overflow: hidden;
      width: 100%;
  }
  .green {
    background: green;
    padding: 50px;
    color: white;
    overflow: hidden;
    width: 100%;
  }
  .black {
    padding: 50px;
    background: black;
    color: white;
    overflow: hidden;
    width: 100%;
  }
  img {
    width: 50%;
  }
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
  </style>
  