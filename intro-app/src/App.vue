<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/to-do">To Do</router-link> |
    <router-link to="/questionare">Questionare</router-link> |
    <router-link to="/buttons">Custom Buttons</router-link>
  </nav>
  <router-view/>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
* {
  box-sizing: border-box;
  margin: 0;
}

a {
    cursor: pointer;
}

nav {
  padding: 30px;
  position: fixed;
  right: 0;
  width: 100%;
  text-align: end;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>