<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
//theme
$pink: #E3D0D8;
$washedLavender: #E7E6F7;
$lavender: #C6D2ED;
$darkPink: #AEA3B0;
$purple: #827081;

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
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
