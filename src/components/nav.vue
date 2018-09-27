<template>
  <nav id="nav" class="navbar is-fixed-top" role="navigation" aria-label="main navigation">
    <div class="link-box">
      <router-link to="/" class="navbar-item">Home</router-link>
      <router-link to="/about" class="navbar-item">About</router-link>
      <img src="../assets/logo.svg" alt="logo" class="logo">
      <router-link to="/projects" class="navbar-item">Projects</router-link>
      <router-link to="/contact" class="navbar-item">Contact</router-link>

      <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false">
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'navBar'
}
</script>

<style lang="scss" scoped>
@import "@/sass/styles.scss";

  #nav {
    background-color: $pink;
    padding: 0;
  }

  .navbar {
    height: 70px;
    display: flex;
    justify-content: center;
  }

  .link-box {
    width: 66%;
    display: flex;
    justify-content: space-between;
  }

  .logo {
    height: 70px;
    padding: 8px;
  }
</style>
