<template>
  <footer class="footer">
    <div class="content columns is-mobile">
      <div class="column icons is-hidden-desktop is-hidden-tablet">
        <a href="https://github.com/garciaryan"><i class="fab fa-github"></i></a>
        <a href="https://www.linkedin.com/in/ryan-garcia-b98b66127/"><i class="fab fa-linkedin-in"></i></a>
        <a href="https://www.facebook.com/ryan.garcia.3705"><i class="fab fa-facebook-square"></i></a>
      </div>
      <div class="column logo-col">
        <img src="../assets/logo.svg" alt="logo" class="logo">
      </div>
      <div class="column">
        <span class="name">rgarciadev<span class="copy">&copy;</span> development</span>
        <div class="address">
          <span>Fresno, CA</span>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'footerBar'
}
</script>

<style lang="scss" scoped>
@import "@/sass/styles.scss";
  .footer {
    height: 15vh;
  }
  .name {
    font-weight: 400;

    .copy {
      font-weight: 300;
    }
  }
  .icons {
    display: flex;
    align-items: center;
    justify-content: space-between;
    a {
      color: $purple;
      font-size: 23px;
    }
  }
  .logo-col {
    justify-content: center;
    align-items: center;
    display: flex;
    .logo {
      height: 50px;
    }
  }

</style>
