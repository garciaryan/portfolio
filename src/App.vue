<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
@import "@/sass/styles.scss";

#app {
  font-family: 'Josefin Sans', sans-serif;
  font-weight: 300;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
